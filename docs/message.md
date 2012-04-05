Publishing messages is declarative and not OO.

Should be using a simple OO wrapper for a deliverable message.

Needs to be an object that can…
    - Set its priority and so on
    - Encode its payload

And then expose itself for "serialization" back out to Rabbit through whatever adapter we're using to send the message.