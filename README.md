# README

Date: August 15th, 2016


1. Run `ember s`
2. Understand the hierarchy of templates. i.e.

```
http://localhost:4200/posts
> posts.hbs > posts.index.hbs
```

```
http://localhost:4200/posts/post
> posts.hbs > post.hbs > post.index.hbs
```


More examples:

1. When `this.route('tag');` without a callback, `index.hbs` wont be invoked.
```
http://localhost:4200/posts/post/tag
> posts.hbs > post.hbs > tag.hbs
```

2. When `this.route('tag', function(){});`, if there is an callback, then `index.hbs` will be invoked.
```
http://localhost:4200/posts/post/tag/
> posts.hbs > post.hbs > tag.hbs > tab.index.hbs
```

## Reference
1. [Rendering a Template](https://guides.emberjs.com/v2.7.0/routing/rendering-a-template/)
