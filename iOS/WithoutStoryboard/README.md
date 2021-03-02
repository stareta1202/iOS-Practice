# Without Storyboard
study for features about iOS and Swift

## start with Scene Delegate 
1. remove general - main interface : main
2. remote storyboard name at info.plist
3. add at SceneDelegate 

``` Swift
    func scene(_ scene: UIScene, willConnectTo session: UISceneSession, options connectionOptions: UIScene.ConnectionOptions) {
        guard let scene = (scene as? UIWindowScene) else {return}
        window = UIWindow(frame: scene.coordinateSpace.bounds)
        window?.windowScene = scene
        window?.rootViewController = SceneStartViewController()
        window?.makeKeyAndVisible()
    }

```

