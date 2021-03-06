Introvert
==============
Just a little library that likes sunsets, long walks on the beach, and thinking about your clojurescript.

                                        _   ___...___   _
     _____  _     _  _________  _____  | \ / _______ \ / | _       _  ______  _____  _________
    |_   _|| \   | ||___   ___||  __ \ | .\ //\     \ /. || |     | ||  ____||  __ \|___   ___|
      |.|  |. \  | |    |.|    |.|  \.\ \ .\|/\\     /. / |.|     |.||.|     |.|  \.\   |.|
      | |  | | \ | |    | |    | |__/ / |\ .\  \\   /. /| | \     / || |__   | |__/ /   | |
      |.|  | |\.\| |    |.|    | _. _/  |/ ./  |.\  \. \|  \ \   / / |. __|  | _. _/    |.|
      | |  | | \ | |    | |    | |\ \   / ./   //\\  \. \   \ \ / /  | |     | |\ \     | |
     _|.|_ | |  \ .|    |.|    |.| \.\ | ./\  //  \\//\. |   \ ' /   |.|____ |.| \.\    |.|
    |_____||_|   \_|    |_|    |_|  \_\|_/\ \|/____\/ /\_|    \_/    |______||_|  \_\   |_|
                                           \_________/


## Functions
(**->js** **obj**:any _[**flatten**:bool = false]_) - Converts an arbitrary cljs data structure into a native JS approximation. Capable of handling atoms, circular references, and most other complications that naive implementations tend to barf on. Works best paired with intelligent dev tools (such as those provided by webkit) To serialize the object (e.g. to display it as a string), you will need to flatten it to remove circular references.

(**deep=** **value1**:any **value2**:any) - Equality comparator with support for value-comparisons between raw JS objects and arrays. Also retains compatibility with cljs value equality (though it incurs a little bit of overhead).

## Changelog
* 0.1.5 Improves code style courtesy of @jamii.
* 0.1.4 Adds support for converting whole namespaces with `->js`.
* 0.1.3 Adds preliminary deep=, Fixes dropped support for vectors and botched test cases.
* 0.1.2 Refines `->js` to support anything supporting ISeq, IPersistentMap, or IPersistentSet.
* 0.1.1 Adds support for flattening circular references.
* 0.1.0 Initial Release.
