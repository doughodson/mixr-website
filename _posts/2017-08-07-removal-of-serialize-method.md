---
layout: post
title:  "Poll! Removal of serialize() Method from Class Definitions?"
---
All MIXR classes include a method called serialize() that can be used to write and save object state data associated with input configuration parameters (i.e., slots). Using this feature, in theory, a subset of state data for each created object within an executing simulation application could be recorded and used to reset or restart an application at any given time with a degree of precision - a 'checkpoint' of sorts.

While this feature is interesting and potentially very useful in certain situations, it does require additional effort from a developer to understand its role and fully define serialization behavior for each and every class. This includes the semantics of what is intended by a 'reset' or 'restart' - which is not always entirely clear, as it often depends on the purpose. Because of this, it is believed that many developers simply don't define anything (i.e., leave the method empty) or redefine it (if already defined) to do what they want.

Given this situation and the understanding that no one is even using this feature, we are considering removing this aspect of object functionality from the code base to reduce code size and overall complexity.

This post solicits feedback from the community on this topic. If you feel strongly about retaining this feature, please send an email or post a comment on the forum. If we don't hear anything within a reasonable amount of time, this method (and capability) will most likely be removed in favor of simplicity.
