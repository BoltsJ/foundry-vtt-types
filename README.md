# (Inofficial) Foundry VTT Types

<div align=center>

[![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

</div>

## Introduction

This was originally created by @NickEastNL for his Project Creator over on
[GitLab](https://gitlab.com/foundry-projects/foundry-pc/foundry-pc-types). This
fork is an attempt to update the types to 0.7.9 of Foundry and to provide better
maintenance.

## Installing

```bash
npm install --save-dev github:kmoschcau/foundry-vtt-types
```

## Configuration

Add the project to your types section in your `tsconfig.json`:

```json
{
  "compilerOptions": {
    "types": [
      "foundry-vtt-types"
    ]
  }
}
```

## Contributing

The work for enhancing this to the current Foundry version is done in the
`foundry-0.7.9` branch. Merge requests for splitting up the work are welcome,
otherwise I will just work through this from top to bottom of the original
foundry.js file.

# What follows is the original README.

<div align=center>

# Foundry Project Creator Types

[![Chat on Discord](https://img.shields.io/discord/520640779534729226?style=flat-square&label=discord&logo=discord)](https://discord.gg/59Tz2X7)
[![Twitter Follow](https://img.shields.io/badge/follow-%40NickEastNL-blue.svg?style=flat-square&logo=twitter)](https://twitter.com/NickEastNL)
[![Become a Patron](https://img.shields.io/badge/support-patreon-orange.svg?style=flat-square&logo=patreon)](https://www.patreon.com/nick_east)
[![Donate via Ko-Fi](https://img.shields.io/badge/support-ko--fi-ff4646?style=flat-square&logo=ko-fi)](https://ko-fi.com/nickeast)

</div>

**Unfortunately due to circumstances the type definitions are not up-to-date with the most recent versions of Foundry VTT. Other parties are working on more efficient methods to create type definitions which may hopefully replace this. The size of the API and the frequent updates combined with my own changed plans make it too difficult to provide the full type definitions. I have decided therefore to focus on the definitions I require for my work and leave it in the hands of people more capable than me to provide better definitions.**

This package provides type definitions for the Foundry VTT API, useful for both vanilla JS and TypeScript to get autocomplete, Intellisense, and type checking.

Unlike other packages, this will gradually be updated as I add more type definitions. Therefore, I will not use version numbers and tags to tag releases.

Considering the size of the Foundry API and the frequent changes to it, please be aware that not all types may be accurate. If in doubt, double-check to make sure what you're attempting to do is possible (such as by temporarily disabling typechecking). If types are missing, outdated, or otherwise incorrect, please report it in the Issue Tracker.

### Contributions

~~Due to the difficulty of managing different Merge Requests and ensuring all contributions follow the standards of this repository, it is no longer possible to submit Merge Requests directly. Instead it is now recommended to use Issue reports only to inform us about missing or incorrect types.~~

~~When posting an Issue, please ensure you mention which version of Foundry you are using, as well as as much information about the correct types as possible, preferably the line numbers and suggestions for the signature.~~

**As explained above, I anticipate no more complete updates other than the types I need. Therefore, it's highly ulikely suggestions and issues will be handled.**

## Installing

Due to how the Node Package Manager (NPM) works, it is not possible to simply update a package installed from Git using `npm install`. Simply reinstall the package with the command below to retrieve the latest version.

```
npm install --save-dev gitlab:foundry-projects/foundry-pc/foundry-pc-types
```

When using the CLI ([Foundry Project Creator](https://gitlab.com/foundry-projects/foundry-pc/create-foundry-project)), it will add this package to your project by default, and configure the `tsconfig.json` and add the above command as an npm script for you.

## Configuration

When not using my Project Creator, you need to manually configure your project to use the types.

TypeScript is configured with a `tsconfig.json` file in your project root. Add the following property to enable TS to use the Foundry API typings.

```json
{
	"compilerOptions": {
		"types": "foundry-pc-types"
	}
}
```

For vanilla JavaScript, you may need to use `jsconfig.json` with the above configuration, or allow TypeScript to also parse JavaScript files. Please refer to the documentation of your IDE and/or TypeScript to learn how to properly configure your environment.

## Support

All the work that I do for Foundry I do in my spare time. If you love using it, please consider supporting me through either [Patreon](https://www.patreon.com/nick_east) or [Ko-Fi](https://ko-fi.com/nickeast) so that I can continue my work and worry less about life itself.
