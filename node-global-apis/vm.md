# VM (executing JavaScript)
https://nodejs.org/api/vm.html

Table of contents
VM (executing JavaScript)
Class: vm.Script
new vm.Script(code[, options])
script.createCachedData()
script.runInContext(contextifiedObject[, options])
script.runInNewContext([contextObject[, options]])
script.runInThisContext([options])
Class: vm.Module
module.dependencySpecifiers
module.error
module.evaluate([options])
module.identifier
module.link(linker)
module.namespace
module.status
Class: vm.SourceTextModule
new vm.SourceTextModule(code[, options])
sourceTextModule.createCachedData()
Class: vm.SyntheticModule
new vm.SyntheticModule(exportNames, evaluateCallback[, options])
syntheticModule.setExport(name, value)
vm.compileFunction(code[, params[, options]])
vm.createContext([contextObject[, options]])
vm.isContext(object)
vm.measureMemory([options])
vm.runInContext(code, contextifiedObject[, options])
vm.runInNewContext(code[, contextObject[, options]])
vm.runInThisContext(code[, options])
Example: Running an HTTP server within a VM
What does it mean to "contextify" an object?
Timeout interactions with asynchronous tasks and Promises
