Each different publisher/consumer should subclass / delegate off of the core classes, and then be installed globally OR locally to the domain-specific app via an autoloading pattern.

modules/
    __autoload.php (optional - only needed if you need to do something beyond the generic pattern)
    consumers/
    producers/
    vhosts/
        {TYPE}
        …
    
    exchanges/
        {TYPE}
        …
    
    queues/
        {TYPE}
        …
    
    tests/

Each of those directories then map to calling a global Factory registry registering the configurations, and then making it available to the outside code.