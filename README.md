# videojs-ass-es6

Add **Advanced SubStation Alpha (ASS)** subtitles support to
[videojs](https://github.com/videojs/video.js) using the
[libjass](https://github.com/Arnavion/libjass) library.


## Install

For plugin that supports videojs v5.x install using either:

- `yarn add videojs-ass-es6`
- `npm install videojs-ass-es6`

## Usage

Initialize the `ass` plugin with the `src` field like the following:

```js
videojs('player_id', {
  plugins: {
    ass: {
      subtitles: [
        {src: 'subs/subtitles.ass', label: 'English', srclang: 'en'}
      ]
    }
  }
});
```

| Option      | Default       | Description                                                |
| ----------- | ------------- | ---------------------------------------------------------- |
| src         | -<sup>1</sup> | `.ass` / `.ssa` source.                                    |
| label       | -<sup>2</sup> | subtitle track label that shows up in the subtitles picker |
| label       | -<sup>3</sup> | subtitle language code                                     |

**Footnotes:**

1. This property is required!
2. Has fallback values but you should provide a better label.
3. Should be the 2 character language code of the subtitle
