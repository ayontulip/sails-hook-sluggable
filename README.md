# sails-hook-sluggable


Easy creation of slugs for your Waterline models in Sails

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
      from: "first_name,middle_name,last_name",     //default 'title'
      defaultField: "full_name",                    //default null
      multiField: true,                             //default false
      defaultValue: "slug",                         //default 'slug'
      remove : null,                                //default null
      lower : true,                                 //default 'true
      separator : "-",                              //default '-'
    }
