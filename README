Slim PHP Mongo REST server
==========================

MongoDB REST server using Slim PHP

Requirements
============

PHP, with MongoDB driver
http://php.net/manual/en/mongo.installation.php

A web server such as nginx, lighttpd or Apache httpd

Usage
=====

Configure MONGO_HOST at the top of index.php

Here's some jQuery -

Fetch collection
----------------

Get all in collection (respecting limit set in mongo-list.php)
    
```javascript
$.get(
  '/database/collection',
  function(data) {
    console.log(data);
  }
);
```

Get blogs with phone in the title

```javascript
$.get(
  '/database/collection',
  {
    filter: {
      type: 'blogs'
    },
    wildcard: {
      title: 'phone'
    }
  },
  function(data){
    console.log(data);
  }
);
```

And in Backbone

```javascript
var collection = Backbone.Collection.extend({
  url: '/database/collection'
});

collection.fetch({
  data: {
    filter: {
      type: 'blogs'
    }
    // etc.
  }
});
```

Save document
-------------

```javascript
$.ajax({
  url: '/database/collection',
  type: 'POST',
  contentType: 'application/json',
  dataType: 'json',
  data: JSON.stringify({
    title: 'My Object',
    body: 'text'
    // etc.
  }),
  success: function(data) {
    console.log(data);
  },
  error: function (data) {
    console.log(data);
  }
});
```

Update document
---------------

```javascript
$.ajax({
  url: '/database/collection/id',
  type: 'PUT',
  contentType: 'application/json',
  dataType: 'json',
  data: JSON.stringify({
    title: 'My Object',
    body: 'text'
    // etc.
  }),
  success: function(data) {
    console.log(data);
  },
  error: function (data) {
    console.log(data);
  }
});
```

What's coming next
==================

* Save/Update/Delete multiple
* Fast update using save()
* More configurable filter/regex options for listing
