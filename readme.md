# Next-Shynet

A library for integrating [shynet](https://github.com/milesmcc/shynet)
into your [next.js](https://nextjs.org/) project.

It helps to easily use shynet in a single page application.
The library also has declarations for typescript.

## Usage

Install this library:

```bash
npm install next-shynet
```

Change your `_app.js`:

```diff
+import Shynet from "next-shynet"

const YourApp = ({ Component, pageProps }) => {
    return (
        <div>
+           <Shynet
+               scriptSrc="https://your-shynet-instance/.../index.js"
+               imgSrc="https://your-shynet-instance/.../pixel.gif" />
            <Component {...pageProps} />
        </div>
    )
}
```

The link to the tracking pixel is optional.

To prevent the script from being loaded during development,
you can set the `productionOnly` option to `true`.

## How to build

```bash
npm install
npm run build
```

The generated files will be in the `/dist` directory.

## Authors

- Ivan Reshetnikov <ordinarydev@protonmail.com>
