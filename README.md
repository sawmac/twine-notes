# Notes on using Twine/Sugarcube/Tweego

## Resources
* [Twine](https://twinery.org/)
* [Sugarcube 2.0](https://www.motoslave.net/sugarcube/2/)
* [Sugarcube 2.0 Docs](https://www.motoslave.net/sugarcube/2/docs/)
* [Tweego](https://www.motoslave.net/tweego/). Command-line compiler for .twee files so you can work your own IDE to produce Twine adventures.
* [Tweego Docs](https://www.motoslave.net/tweego/docs).

## Tweego Notes
### Installation
* Download: https://www.motoslave.net/tweego/
* Download Sugarcube story-format: 
* Add `TWEEGO-PATH` environment variable to `.bash-profile`
  * `sudo nano ~/.bash_profile`
  * `export TWEEGO_PATH="/Users/dave/Documents/twine/story_formats"`

### Structuring Docs
```
project_directory/
    images/   <-- for images. Use paths relative to project_directory
    src/   <--for .twee files, .css and .js
```

### Compile
Compile within the project_directory folder -- create an index.html file at that level: `tweego -o index.html src`

Recompile when src changes:
`tweego -o index.html src --watch`

Display debugger:
`tweego -o index.html src --test`