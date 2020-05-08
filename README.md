<div align="center">
    <h1>ngx-hoverscroll</h1>
    <p>Angular Directive for Scrolling on Hover</p>
    <img src="https://raw.githubusercontent.com/arroyonetworks/ngx-hoverscroll/f3698d0ac7d01bddb67dc67a1dfed6ab28b92b69/docs/hoverscroll.gif">
</div>

## Dependencies

Angular Support

| Version           | Angular Version   |
|:-----------------:|:-----------------:|
| 2.0.0             | 6-7               |
| **2.0.2**         | 6-9               |


No external dependencies other than Angular are required!

## Installation

Install `@arroyo/ngx-hoverscroll` from `npm`:
```bash
> npm install @arroyo/ngx-hoverscroll
```


## Setup

Follow the instructions below for adding `ngx-hoverscroll` to your Angular application:

1. Add the Imports to your Module. For example, `app.module.ts`:
    ```typescript
    import { HoverScrollModule } from '@arroyo/ngx-hoverscroll';
    ...
    
    @NgModule({
      ...
      imports: [HoverScrollModule.forRoot(), ... ],
      ... 
    })
    ```
    
2. Add the `hoverScroll` Directive to Your Template:
    ```angular2html
    <div class="site-sidebar">
      <div class="site-sidebar-body" hoverScroll>
        <ul class="site-menu" data-plugin="menu">
           ...
        </ul>
       </div>
    </div>
    ```

At this time, only vertical scrolling is supported.

### Demo App

A demo application is included. It is built with `angular-cli`. To run the demo install `angular-cli` and run:
```bash
> ng serve demo
```

The demo application is found in the `demo/` directory inside projects.


### Advanced Usage

The `hoverScroll` directive selects the immediate child as the "scrolled" content.
The inner container should overflow the outer container in order to provide scrolling content.

One way to accomplish this is to set the outer container to be a max-height of the window and the inner
container to contain it's natural height.

See the demo app for a working example.


#### Options

The directive takes the following inputs:

- ``scrollBuffer (number)`` Added scroll buffer on the top/bottom of the container. Default: 0px.
- ``stableBuffer (number)`` Buffer on mouse entry that the cursor must traverse before scrolling. Default: 25px.


## Contributing

By submitting a pull request or changes for this project, you agree to license your contribution
under the MIT license to this project.

To ensure that you have the ability to publish your changes under our licensing requirements, we require
that you, as the patch provider, provide a Sign-off, which provided, means that you have the necessary permissions or have been
granted the permissions to provide the offered code or patches. 

As an author, please sign your commits as often as possible using your published GPG key.

## License

MIT License

Copyright (c) 2017 Arroyo Networks, LLC <br>
Copyright (c) 2020 Arroyo Networks, Inc.
