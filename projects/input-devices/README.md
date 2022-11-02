# input devices

So i've started playing around with different form's of input devices. Mainly a split keyboard and a trackball. I'd like to build a roller mouse next, as it seems interesting

## ferris sweep split keyboard (34 keys)

in the qmk_firmware repo, build using

> ./util/docker_build.sh ferris/sweep:emile

## trackball

I've retrofitted it with ceramic bearings, as the past ones were really unprecise.

A thing I wasn't really aware of before using the trackball: how inprecise it can be for small movements. Large movements are amazing, but if you want to move the cursor one or two characteres to the side, it doesn't really work out.

A test I'd propose you to do when using a trackball, is to place a single finger on the top of the ball and try to move the mouse as little as possible in one direction. The distance the mouse "hops" is the score it get's (less is better). Changing the bearings to higher quality ones has helped a lot in that regard.
