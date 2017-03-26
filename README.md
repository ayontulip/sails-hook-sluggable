# Sails unique slugs


Easy to create unique slugs for your Waterline models in Sails

## Installation

Add this hook to your Sails app:

```shell
$ npm install sails-hook-sluggable
```

That's all!

## Usage

Add an attribute of type `slug` in a model:

```js
module.exports = {

  attributes: {
    title: {
      type: 'string',
      required: true,
      unique: true
    },
    content: {
      type: 'text'
    },
    name: {
      type: 'string'
    },
    slug: {
      type: 'slug',
      from: 'title',
      unique: true
    }
  }
};


## Parameters

    username: {
      type: 'slug',
      from: "first_name,last_name",     // Field name for generate Slug, default 'title'
      defaultField: "full_name",        // IF `from` value null than use Field, default null
      multiField: true,                 // Use multi Field for generate Slug, default false
      defaultValue: "slug",             // If Fields are null default string, default 'slug'
      remove : null,                    // (optional) regex to remove characters, default null
      lower : true,                     // result in lower case, default 'true
      separator : "-",                  // replace spaces with replacement, default "-"
    }
