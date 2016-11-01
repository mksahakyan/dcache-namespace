[![Build status](https://travis-ci.org/dcache-elements/dcache-namespace.svg?branch=master)](https://travis-ci.org/dcache-elements/dcache-namespace)

_[Demo and API docs](https://dcache-elements.github.io/dcache-namespace/components/dcache-namespace/)_

# \<dcache-namespace\>

dcache-namespace can be used to perform an ajax call to dcache using 
dcache-restful api.

An example of how to use dcache-namespace to create a new directory 
inside dcache:

```html
<dcache-namespace id="namespace"></dcache-namespace>
```
...

```javascript
    var namespace = document.getElementById('namespace')

    //supply credential
    namespace.auth = 'YW5vbnltb3VzOm5vcGFzc3dvcmQ';

    namespace.promise.then(
        function(req) {
            //Successful - do something 
        }
    ).catch(
        function(err) {
            //Fail - do something
        }
    );

    namespace.mkdir({
      url: '/api/v1/namespace/', 
      name: folderName
    });
```

**Task list**

- [ ] add unit test