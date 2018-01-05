## hexo-first

My first hexo plugin

This plug in just adds an example hexo tag that is the same as just having a script in the scripts folder of the hexo project that has this in it:

```js
hexo.extend.tag.register('first_plugin', function(){
 
    return '<p>This is my first hexo plugin.</p>';
 
});
```

At which point it can be used in a markdown file like this:

```
{% first_plugin %}
```

## Manual install process

Because I will not be publishing this, and many other plugins like this I must follow the manual install process that involves changing the current working dir to the node_modules folder of the hexo project and cloning this in

```
$ cd node_modules
$ git clone https://github.com/dustinpfister/hexo-first
```
I will then need to add it to the package.json of the porject as well.

```js
{
  "name": "hexo-site",
  "version": "0.0.0",
  "private": true,
  "hexo": {
    "version": "3.4.4"
  },
  "dependencies": {
    "hexo": "^3.2.0",
    "hexo-generator-archive": "^0.1.4",
    "hexo-generator-category": "^0.1.3",
    "hexo-generator-index": "^0.2.0",
    "hexo-generator-tag": "^0.2.0",
    "hexo-renderer-ejs": "^0.3.0",
    "hexo-renderer-stylus": "^0.3.1",
    "hexo-renderer-marked": "^0.3.0",
    "hexo-server": "^0.2.0",
    "hexo-first": "^0.0.0"
  }
}
```