# Web Streams API
https://nodejs.org/api/webstreams.html

Table of contents
Web Streams API
Overview
Example ReadableStream
API
Class: ReadableStream
new ReadableStream([underlyingSource [, strategy]])
readableStream.locked
readableStream.cancel([reason])
readableStream.getReader([options])
readableStream.pipeThrough(transform[, options])
readableStream.pipeTo(destination, options)
readableStream.tee()
readableStream.values([options])
Async Iteration
Transferring with postMessage()
Class: ReadableStreamDefaultReader
new ReadableStreamDefaultReader(stream)
readableStreamDefaultReader.cancel([reason])
readableStreamDefaultReader.closed
readableStreamDefaultReader.read()
readableStreamDefaultReader.releaseLock()
Class: ReadableStreamBYOBReader
new ReadableStreamBYOBReader(stream)
readableStreamBYOBReader.cancel([reason])
readableStreamBYOBReader.closed
readableStreamBYOBReader.read(view)
readableStreamBYOBReader.releaseLock()
Class: ReadableStreamDefaultController
readableStreamDefaultController.close()
readableStreamDefaultController.desiredSize
readableStreamDefaultController.enqueue(chunk)
readableStreamDefaultController.error(error)
Class: ReadableByteStreamController
readableByteStreamController.byobRequest
readableByteStreamController.close()
readableByteStreamController.desiredSize
readableByteStreamController.enqueue(chunk)
readableByteStreamController.error(error)
Class: ReadableStreamBYOBRequest
readableStreamBYOBRequest.respond(bytesWritten)
readableStreamBYOBRequest.respondWithNewView(view)
readableStreamBYOBRequest.view
Class: WritableStream
new WritableStream([underlyingSink[, strategy]])
writableStream.abort([reason])
writableStream.close()
writableStream.getWriter()
writableStream.locked
Transferring with postMessage()
Class: WritableStreamDefaultWriter
new WritableStreamDefaultWriter(stream)
writableStreamDefaultWriter.abort([reason])
writableStreamDefaultWriter.close()
writableStreamDefaultWriter.closed
writableStreamDefaultWriter.desiredSize
writableStreamDefaultWriter.ready
writableStreamDefaultWriter.releaseLock()
writableStreamDefaultWriter.write([chunk])
Class: WritableStreamDefaultController
writableStreamDefaultController.abortReason
writableStreamDefaultController.error(error)
writableStreamDefaultController.signal
Class: TransformStream
new TransformStream([transformer[, writableStrategy[, readableStrategy]]])
transformStream.readable
transformStream.writable
Transferring with postMessage()
Class: TransformStreamDefaultController
transformStreamDefaultController.desiredSize
transformStreamDefaultController.enqueue([chunk])
transformStreamDefaultController.error([reason])
transformStreamDefaultController.terminate()
Class: ByteLengthQueuingStrategy
new ByteLengthQueuingStrategy(options)
byteLengthQueuingStrategy.highWaterMark
byteLengthQueuingStrategy.size
Class: CountQueuingStrategy
new CountQueuingStrategy(options)
countQueuingStrategy.highWaterMark
countQueuingStrategy.size
Class: TextEncoderStream
new TextEncoderStream()
textEncoderStream.encoding
textEncoderStream.readable
textEncoderStream.writable
Class: TextDecoderStream
new TextDecoderStream([encoding[, options]])
textDecoderStream.encoding
textDecoderStream.fatal
textDecoderStream.ignoreBOM
textDecoderStream.readable
textDecoderStream.writable
Utility Consumers
streamConsumers.arrayBuffer(stream)
streamConsumers.blob(stream)
streamConsumers.buffer(stream)
streamConsumers.json(stream)
streamConsumers.text(stream)
