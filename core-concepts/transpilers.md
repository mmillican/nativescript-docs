---
title: Transpilers
description: Learn how to enable TypeScript and other transpiler support in your project.
position: 8
slug: transpilers
previous_url: /transpilers
---

# Using transpilers in NativeScript

Transpilers allow you to develop your application in languages other than JavaScript, CSS and XML. NativeScript applications can be developed more comfortably when transpilers are used in the project. NativeScript projects support two transpilers out-of-the-box - TypeScript and Babel, although any other transpiler can be integrated through the necessary hooks.

## Installing TypeScript

Run the following command to install TypeScript support into your project:

```Shell
tns install typescript
```

The above command installs the TypeScript compiler and the `nativescript-dev-typescript` npm module as dev dependencies. The latter installs the necessary `prepare` and `livesync` hooks into your project, so that the TypeScript files in your project are automatically transpiled during build and when live-syncing.

It also creates a `tsconfig.json` file in the root of your project that contains the compiler configuration. You can edit it to change the configuration.

If you want to change the version of the TypeScript compiler used in your project, simply install the version you want into your project through npm.

## Installing Babel

Run the following command to install Babel support into your project:

```Shell
tns install babel
```

The above command installs the Babel compiler and the `nativescript-dev-babel` npm module as a dev dependencies. The latter installs a `prepare` hook into your project, that transpiles your JavaScript files with Babel during build and when live-syncing.

If you want to change the version of the Babel compiler used in your project, simply install the version you want into your project through npm.

If you want to configure Babel, create a `.babelrc` file in the root of your project according to [spec](https://babeljs.io/docs/usage/babelrc/).

## Installing XML validation against XSD schema

Run the following command to install XML validation against XSD schema into your project:

```Shell
tns install xmlxsd
```

The above command installs the `nativescript-dev-xmlxsd` npm module as a dev dependencies. The latter installs a `prepare` hook into your project, that validates your XML files against NativeScript XSD schema during build and when live-syncing.

If you want to change the version of the XML validation against XSD schema used in your project, simply install the version you want into your project through npm.

## Installing Less CSS pre-processor

Run the following command to install Less CSS pre-processor into your project:

```Shell
tns install less
```

The above command installs the `nativescript-dev-less` npm module as a dev dependencies. The latter installs a `prepare` hook into your project, that converts your *.less files to *.css files during build and when live-syncing.

If you want to change the version of the Less CSS pre-processor used in your project, simply install the version you want into your project through npm.

For more info about Less CSS pre-processor please visit http://lesscss.org/.

## Installing Jade

Run the following command to install Jade language support into your project:

```Shell
tns install jade
```

The above command installs the `nativescript-dev-jade` npm module as a dev dependencies. The latter installs a `prepare` hook into your project, that converts your *.jade files to *.xml files during build and when live-syncing.

If you want to change the version of the Jade language support used in your project, simply install the version you want into your project through npm.

For more info about Jade language please visit http://jade-lang.com/.

## Installing other transpilers

Transpiler support can be extended through the use of hooks. The easiest way to distribute transpiler hooks is by means of npm modules. You can use the implementation of the TypeScript and Babel hooks as reference and grok the [nativescript-hook module](https://github.com/NativeScript/nativescript-hook) that provides common hook installation support to transpiler authors.
