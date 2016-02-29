# fiercepunchstudios.github.io_middleman #

The source for the site that will be published to fiercepunchstudios.github.io.

## Getting Started ##
Make sure you have git remotes:
1. `origin` set to `https://github.com/FiercePunchStudios/fiercepunchstudios.github.io_middleman.git`
2. `prod` set to `https://github.com/FiercePunchStudios/fiercepunchstudios.github.io`

Test using `bemb` or `bundle execute middleman -b 0.0.0.0`
Publish using `be middleman deploy`

## Dev Notes ##

### Project Generation ###
1. `git clone git://github.com/axyz/middleman-zurb-foundation.git ~/.middleman/zurb-foundation`
2. `middleman init fiercepunchstudios.github.io_middleman --template=zurb-foundation`
3. `cd fiercepunchstudios.github.io_middleman`
4. `bower install`
5. `bower install foundation-icon-fonts`
6. `cd source/bower_components/foundation-icon-fonts/ && mv foundation-icons.css foundation-icons.css.bkp`
7. Add to app.css.scss:
  1. `$fi-path: "../bower_components/foundation-icon-fonts";`
  2. `@import "../bower_components/foundation-icon-fonts/foundation-icons";`
  3. See issue https://github.com/zurb/foundation-icon-fonts/issues/27
