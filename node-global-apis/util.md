# Util
https://nodejs.org/api/util.html

Table of contents
Util
util.callbackify(original)
util.debuglog(section[, callback])
debuglog().enabled
util.debug(section)
util.deprecate(fn, msg[, code])
util.format(format[, ...args])
util.formatWithOptions(inspectOptions, format[, ...args])
util.getSystemErrorName(err)
util.getSystemErrorMap()
util.inherits(constructor, superConstructor)
util.inspect(object[, options])
util.inspect(object[, showHidden[, depth[, colors]]])
Customizing util.inspect colors
Modifiers
Foreground colors
Background colors
Custom inspection functions on objects
util.inspect.custom
util.inspect.defaultOptions
util.isDeepStrictEqual(val1, val2)
util.promisify(original)
Custom promisified functions
util.promisify.custom
Class: util.TextDecoder
WHATWG supported encodings
Encodings supported by default (with full ICU data)
Encodings supported when Node.js is built with the small-icu option
Encodings supported when ICU is disabled
new TextDecoder([encoding[, options]])
textDecoder.decode([input[, options]])
textDecoder.encoding
textDecoder.fatal
textDecoder.ignoreBOM
Class: util.TextEncoder
textEncoder.encode([input])
textEncoder.encodeInto(src, dest)
textEncoder.encoding
util.toUSVString(string)
util.types
util.types.isAnyArrayBuffer(value)
util.types.isArrayBufferView(value)
util.types.isArgumentsObject(value)
util.types.isArrayBuffer(value)
util.types.isAsyncFunction(value)
util.types.isBigInt64Array(value)
util.types.isBigUint64Array(value)
util.types.isBooleanObject(value)
util.types.isBoxedPrimitive(value)
util.types.isCryptoKey(value)
util.types.isDataView(value)
util.types.isDate(value)
util.types.isExternal(value)
util.types.isFloat32Array(value)
util.types.isFloat64Array(value)
util.types.isGeneratorFunction(value)
util.types.isGeneratorObject(value)
util.types.isInt8Array(value)
util.types.isInt16Array(value)
util.types.isInt32Array(value)
util.types.isKeyObject(value)
util.types.isMap(value)
util.types.isMapIterator(value)
util.types.isModuleNamespaceObject(value)
util.types.isNativeError(value)
util.types.isNumberObject(value)
util.types.isPromise(value)
util.types.isProxy(value)
util.types.isRegExp(value)
util.types.isSet(value)
util.types.isSetIterator(value)
util.types.isSharedArrayBuffer(value)
util.types.isStringObject(value)
util.types.isSymbolObject(value)
util.types.isTypedArray(value)
util.types.isUint8Array(value)
util.types.isUint8ClampedArray(value)
util.types.isUint16Array(value)
util.types.isUint32Array(value)
util.types.isWeakMap(value)
util.types.isWeakSet(value)
util.types.isWebAssemblyCompiledModule(value)
Deprecated APIs
util._extend(target, source)
util.isArray(object)
util.isBoolean(object)
util.isBuffer(object)
util.isDate(object)
util.isError(object)
util.isFunction(object)
util.isNull(object)
util.isNullOrUndefined(object)
util.isNumber(object)
util.isObject(object)
util.isPrimitive(object)
util.isRegExp(object)
util.isString(object)
util.isSymbol(object)
util.isUndefined(object)
util.log(string)
