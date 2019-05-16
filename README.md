#### Hook easily like(just copy/paste `CHMethod` line......):

```
CHDeclareClass(UIApplication)
//- (void)openURL:(NSURL*)url options:(NSDictionary<UIApplicationOpenExternalURLOptionsKey, id> *)options completionHandler:(void (^ __nullable)(BOOL success))completion
CHMethod3(void, UIApplication, openURL, id, arg1, options, id, arg2, completionHandler, id, arg3)
{
    SuperCHMethod3(void, UIApplication, openURL, id, arg1, options, id, arg2, completionHandler, id, arg3);
}
CHConstructor{
    @autoreleasepool{
        CHLoadLateClass(UIApplication);
        HookCHMethod3(void, UIApplication, openURL, id, arg1, options, id, arg2, completionHandler, id, arg3);
    }
}
```

#### GET CaptainHook : [https://github.com/rpetrich/CaptainHook](https://github.com/rpetrich/CaptainHook)

