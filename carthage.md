#Carthage instructions

1.	Install Carthage
2. 	Create a Cartfile and type `github "ahmednawar/iOS-Deferred-Deep-Linking-SDK"`
3.	run `carthage update`
4.	In your XCode project, add the framework to your target's Embedded Binaries found at `Carthage/Build/iOS/`

**XCode for some reason doesn't detect the headers automatically, this is not related to our framework in particular (I've seen questions on SO regarding Facebook SDKs)**

Either you do:

1.	target -> Build Settings -> User Header Search Paths = $(SRCROOT)       // recursive.
2.	Set Always Search User Paths = YES
3.	Remove *.frameworks from Sub-Directories to Exclude in Recursive Searches.

or

Put the Absolute path in User Header Search Paths. `$(SRCROOT)/Carthage/Build/iOS/BranchSDK.framework/Headers`

(I'll look later if ther is a better way to do this)
