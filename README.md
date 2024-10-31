# ClipGradient
A LuaU module for clipping a UIGradient

Created in for a niche use-case in particular, where due to the limited behavior of a UIGradient object, required the ability to cut off the fade of a UIGradient early (i.e. a gradient moving across a healthbar, it would need to be clipped based on the ratio of health so that it did not pass the edge of the healthbar). Originally created to use for a specific animation in regards to UIGradients.

module:Clip(gradient, clipRatio, offset) --takes @gradient (UIGradient), 
                                                 @clipRatio (Number) -- a number between 0 to 1,
                                                 @offset(Number) -- a number to offset the starting position

                                                 Clips the given UI gradient based on the given ratio and offset.

module:TrackGradient(gradient) -- takes @gradient(UIGradient)

                                  Stores the original gradient's transparency for later references



Ensure :TrackGradient() is called with the UIGradient as a parameter before applying the :Clip() function.
