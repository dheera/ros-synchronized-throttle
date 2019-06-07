# ros-synchronized-throttle

This package is designed to be a replacement for topic_tools/throttle but for when you need to throttle 2 topics in a synchronized fashion, e.g. a left/right stereo pair or RGB/depth that are published to 2 topics with identical timestamps.

It is not restricted to Image types, but it is restricted to types that have a header containing a timestamp. You can perform synchronized throttling on an Image and a PointCloud2 for example, or Image and TwistStamped, but you cannot do it on an Image and Twist, since Twist does not have a header.


