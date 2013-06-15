windowAnimationSample
=====================

Titanium window Custom Animation Sample

In Android, Titanium windows can be heavyweight or lightweight:

 

- A heavyweight window is associated with a new Android Activity. Creating a heavyweight window always creates a new JavaScript context.

 

- A lightweight window is a fullscreen view, and runs in the same Android Activity as the code that created it. Creating a lightweight window creates a new JavaScript context if it was created with the 'url' property set. 
Heavyweight Window Transitions in Android

Heavyweight windows are their own Android Activity. 

The only way to animate the opening of an Activity in Android is to apply an animation resource to it. Passing a Titanium.UI.Animation object as a parameter to open will have no effect if the window being opened is heavyweight and thus opens its own Activity.

 

Instead, in the parameter dictionary you pass to open, you should set the activityEnterAnimation and activityExitAnimation keys to animation resources. 

 

    The activityEnterAnimation should be set to the animation you want to run on the new window (activity) 

    The activityExitAnimation should be set to the animation you want to run on the window (activity) that you are leaving as you open the new heavyweight window above it.
