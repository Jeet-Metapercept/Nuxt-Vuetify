# Nuxt vs Next

The comparison is based on:

-   Popularity (GitHub Stars and npm downloads).
-   Basic Hello World app.
-   Advantages.
-   Disadvantages.
-   Performance.
-   Community involvement.

---

## Next
[GitHub Stars: +53.6k](https://github.com/vercel/next.js)
Next is the most popular framework compared NuxtJs. It has more npm weekly downloads, GitHub stars and number of contributors.

Next.js is a React framework that lets you build server-side rendering and static web applications using React.

## Advantages

-   Every component is server-rendered by default
-   Automatic code splitting for faster page loads
-   Unnecessary code is not loaded
-   Simple client-side routing (page-based)
-   Webpack-based dev environment which supports Hot Module Replacement (HMR)
-   Fetching data is very simple
-   Can be implemented with Express or any other Node.js HTTP server
-   It’s possible to customize with your own Babel and Webpack configurations
-   Easy to deploy anywhere if Node.js is supported
-   Built-in handling of search engine optimization (SEO) for pages

## Disadvantages
-    Next.js is not backend; if you need backend logic, such as a database or an accounts server, you should keep that in a separate server application
 -   Next is powerful, but If you’re creating a simple app, it can be overkill
 -   All data needs to be loadable from both the client and server
    Migrating a server-side app to Next.js is not a quick process, and depending on your project it may be too much work


## Performance

Based on boilerplate app

- [NextJs Benchmark](https://images.ctfassets.net/hspc7zpa5cvq/5gcP7k5WIw7h4mSYuZIDMq/898ad62724d65c969e60d305e1e85d2e/next.png)

- [Lighthouse Score](https://images.ctfassets.net/hspc7zpa5cvq/6SWp0mED1Nb9fXIBM7WwXC/4982654aa94d5d89fc6a0053b1ed90d1/next1.png)

## Sample

[NextJs Sample](https://example-frontend-next-js.sanity-io.now.sh/)
[NextJs Tooling](https://sample-next-app.fabrique.social.gouv.fr/)

---

## Nuxt
[GitHub Stars: +30.4k](https://github.com/nuxt/nuxt.js)

Nuxt is a Vue.js Meta Framework to create complex, fast, and universal(SSR) web applications <b>quickly</b>quickly.
[Features](https://github.com/nuxt/nuxt.js#features)

## Advantages

-    Its main scope is UI rendering, while abstracting away the client/server distribution
-    Statically render your Vue apps and get all of the benefits of a universal app without a server
-    Get automatic code splitting (pre-rendered pages)
-    Setup via the command line with the starter template
-    Get great project structure by default
-    Easily set up transitions between your routes and write single file components
-    Get ES6/ES7 compilation without any extra work
-    Get set up with an auto-updating server for easy development
-    Powerful Routing System with Asynchronous Data
-    Static File Serving
-    ES6/ES7 Transpilation
-    Hot module replacement in Development
-    Pre-processor: Sass, Less, Stylus, etc.

## Disadvantages

-    Lack of some common solid plugins/components. (Google maps, calendar, vector maps). Some components for that exist, but they are generally not very well maintained.
-    It is necessary to go deep in more complex components/plugins. If you want to develop something very flexible, you have to get down to render functions/jsx to do that. (e.g render the contents of a slot in another place/component).
-    Props have to be specified explicitly. There might be cases when you want to transform some CSS classes to props; you’ll have to specify these props or use $attrs / render functions or jsx.
-    High traffic may put strain on your server
-    You can only query and manipulate the DOM in certain hooks

## Performance

Based on boilerplate app

- [NuxtJs Benchmark](https://images.ctfassets.net/hspc7zpa5cvq/77aAB8VVmQi8Kif9gTCQ4U/2fd522c337487dce659994e37e8edbeb/nuxt.png)

- [Lighthouse Score](https://images.ctfassets.net/hspc7zpa5cvq/7hS5nyqzb8UAFd9NidP5sQ/e0cf7d7936142535c0c8aedaad038d81/nuxt1.png)
