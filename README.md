# HTTPRequestResponse
Http request and response in json or xml

- (void)viewDidLoad {
    [super viewDidLoad];
    // Do any additional setup after loading the view, typically from a nib.
    
    NSDictionary *mapData = [[NSDictionary alloc] initWithObjectsAndKeys: @"ravi", @"data",nil];
    
    [[HttpManager sharedManager] requestWithParameter:mapData handler:^(NSDictionary *result, NSError *error) {
        NSDictionary *dict = result;
        NSLog(@"%@",dict);
        
    }];
    
}
