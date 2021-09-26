[LIVR](https://livr-spec.org/)
# Language Independent Validation Rules (v2.0)

## Validator meets the following requirements:
- Rules are declarative and language independent
- Any number of rules for each field
- Validator should return together errors for all fields
- Exclude all fields that do not have validation rules described
- Possibility to validate complex hierarchical structures
- Easy to describe and understand validation
- Returns understandable error codes (neither error messages nor numeric codes)
- Easy to implement own rules (usually you will have several in every project)
- Rules should be able to change results output ("trim", "nested_object", for example)
- Multipurpose (user input validation, configs validation, contracts programming etc)
- Unicode support


## Rules Examples
Simple registration data [(demo)](https://livr-spec.org/introduction/examples.html)

{
    name: 'required',
    email: ['required', 'email'],
    gender: { one_of: ['male', 'female'] },
    phone: {max_length: 10},
    password: ['required', {min_length: 10} ]
    password2: { equal_to_field: 'password' }
}
'required' is a shorter form of { 'required': [] }
{max_length: 10} is a shorter form of {max_length: [10]}
See "How it works" section
Simple validation of nested object (demo)

{
    name: 'required',
    phone: {max_length: 10},
    address: { 'nested_object': {
        city: 'required',
        zip: ['required', 'positive_integer']
    }}
}
{nested_object: {}} is a shorter form of {nested_object: [{}]}
See "How it works" section
Simple list validation (demo)

{
    order_id: ['required', 'positive_integer'],
    product_ids: { 'list_of': [ 'required',  'positive_integer' ] }
}
Validating list of objects (demo)

{
    order_id: ['required', 'positive_integer'],
    products: [ 'not_empty_list', { 'list_of_objects': {
        product_id: ['required','positive_integer'],
        quantity: ['required', 'positive_integer']
    }}]
}
Validating list of different objects (demo)

{
    order_id: ['required', 'positive_integer'],
    products: ['required', { 'list_of_different_objects': [
        'product_type', {
            material: {
                product_type: 'required',
                material_id: ['required', 'positive_integer'],
                quantity: ['required', {'min_number': 1} ],
                warehouse_id: 'positive_integer'
            },
            service: {
                product_type: 'required',
                name: ['required', {'max_length': 10} ]
            }
        }
    ]}]
}
Output modification

{
    email: ['trim', 'required', 'email', 'to_lc']
}
"trim" removes leading and trailing spaces. (skips empty values and object references)
"to_lc" transforms string to lower case. (skips empty values and object references)
You can create pipeline with any modifiers you like.


## Validation Rules
Be aware that all standard rules just skip checking empty values.
So, empty string will pass next validation - "first_name: { min_length: [10] }". We have special rules "required" and "not_empty" to check that value is present.
This allows us to use the same rules for not required fields.

first_name: { min_length: [10] } # name is optional. We will check length only if "first_name" was passed
first_name: [ 'required', { min_length: [10] } ] # check that the name is present and validate length

Standard rules that should be supported by every implementation:
### Common Rules
- required
- not_empty
- not_empty_list
- any_object
### String Rules
- string
- eq
- one_of
- max_length
- min_length
- length_between
- length_equal
- like
### Numeric Rules
- integer
- positive_integer
- decimal
- positive_decimal
- max_number
- min_number
- number_between
### Special Rules
- email
- url
- iso_date
- equal_to_field
### Metarules
- nested_object
- list_of
- list_of_objects
- list_of_different_objects
- or
### Modifiers (previously - "Filter rules")
- trim
- to_lc
- to_uc
- remove
- leave_only
- default




































