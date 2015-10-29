# SonicSonic
Ultrasonic communication.

```objc
- (void)viewDidLoad {
   [super viewDidLoad];
   
   _sonic = [SSSonicSonic sonic];
   _sonic.delegate = self;
   [_sonic subscribe]; // Start Subscription
   
   [self publishSomeSignal]; // Publish Something!
}
 
- (void)sonic:(SSSonicSonic *)sonic didReceiveSignal:(NSString *)signal {
   NSLog(@"Received: %@", signal);
}
 
- (void)publishSomeSignal {
   [_sonic publish:@"Hello World!"];
}
```
