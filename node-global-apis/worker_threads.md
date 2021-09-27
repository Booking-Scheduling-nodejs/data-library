https://nodejs.org/api/worker_threads.html

Table of contents
Worker threads
worker.getEnvironmentData(key)
worker.isMainThread
worker.markAsUntransferable(object)
worker.moveMessagePortToContext(port, contextifiedSandbox)
worker.parentPort
worker.receiveMessageOnPort(port)
worker.resourceLimits
worker.SHARE_ENV
worker.setEnvironmentData(key[, value])
worker.threadId
worker.workerData
Class: BroadcastChannel extends EventTarget
new BroadcastChannel(name)
broadcastChannel.close()
broadcastChannel.onmessage
broadcastChannel.onmessageerror
broadcastChannel.postMessage(message)
broadcastChannel.ref()
broadcastChannel.unref()
Class: MessageChannel
Class: MessagePort
Event: 'close'
Event: 'message'
Event: 'messageerror'
port.close()
port.postMessage(value[, transferList])
Considerations when transferring TypedArrays and Buffers
Considerations when cloning objects with prototypes, classes, and accessors
port.ref()
port.start()
port.unref()
Class: Worker
new Worker(filename[, options])
Event: 'error'
Event: 'exit'
Event: 'message'
Event: 'messageerror'
Event: 'online'
worker.getHeapSnapshot()
worker.performance
performance.eventLoopUtilization([utilization1[, utilization2]])
worker.postMessage(value[, transferList])
worker.ref()
worker.resourceLimits
worker.stderr
worker.stdin
worker.stdout
worker.terminate()
worker.threadId
worker.unref()
Notes
Synchronous blocking of stdio
Launching worker threads from preload scripts