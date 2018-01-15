<!--
title: 13 - How to use semantic versioning
featured: true
-->

# How to use Semantic Versioning

<iframe src="https://www.youtube.com/embed/kK4Meix58R4" frameborder="0" allowfullscreen></iframe>

It's important to communicate the extent of changes in a new release of code, because sometimes updates can break code that a package needs (called *dependencies*).**Semantic versioning** (semver) is a standard that was designed to solve this problem.

## Semver for Publishers

If a project is going to be shared with others, it should start at `1.0.0`, (though some projects on npm don't follow this rule).

After this, changes should be handled as follows:

| CODE STATUS  | STAGE | RULE | EXAMPLE # |
| :----------- | :---- | :--- | :-------- |
| First Release | New Product | Start with 1.0.0 | 1.0.0 |
| Bug fixes, other minor changes | Patch Release | Increment the third digit | 1.0.1 |
| New features that don't break existing features | Minor Release | Increment the middle digit | 1.1.0 |
| Changes that break backward compatibility | Major Release | Increment the first digit | 2.0.0 |

## Semver for Consumers

As a consumer, you can specify which kinds of updates your app can accept in the `package.json` file.

If you were starting with a package 1.0.4, this is how you would specify the ranges:

* Patch releases: `1.0` or `1.0.x` or `~1.0.4`
* Minor releases: `1` or `1.x` or `^1.0.4`
* Major releases: `*` or `x`

## Learn More

For more about using semantic versioning with package.json files, see [Chapter 5](https://docs.npmjs.com/getting-started/using-a-package.json#specifying-packages).

For another way to label releases, learn about [npm dist tags](https://docs.npmjs.com/cli/dist-tag), and [how they relate to semantic versioning](https://docs.npmjs.com/getting-started/using-tags).
