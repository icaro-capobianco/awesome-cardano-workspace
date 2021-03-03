
# What is this?
- A pnpm workspace
- A monorepo with git submodules
- A reference to awesome projects related to cardano

## What does it do?
As a workspace, it allows the development of libraries and projects at the same time, so you can install a library on `/libraries` directory as a dependency to your project, preferably kept at `/projects`

As a monorepo it aggregates many libraries and projects of the community in one place.

## How does it work?
Once you run `pnpm install`, it's going to check on the workspace directories `/libraires` and `/projects` for the existing dependencies, if it finds it, instead of installing the dependency from npm it's going to create a symlink (shortcut) on your /node_modules linking to that package path. So you can develop both at the same time.

As a monorepo it just has a bunch of submodules which I am going to maintain for the community.

*Although it's called a monorepo all the other projects will be kept as submodules, so not I won't be copying people's code over, that would be ridiculous.

# Getting started

You'll need pnpm
https://pnpm.js.org/en/installation

Fork, clone, whatever you want then:

Pull all repos
```
git submodule update --init --recursive
```

Install stuff
```
pnpm install
```

# Add your project or library

To add your project

**\*dir name has to be the same as package name in package.json**
```
git submodule add (repo-uri) projects/package-name
```

To add your library
```
git submodule add (repo-uri) libraries/package-name
```

# Why pnpm?
I tried many workspace tools and these were the results.

**yarn**

Used to be my favorite until yarn v2 started to require you to keep their binary file in your codebase (https://github.com/yarnpkg/berry/issues/2474)

**npm**

npm workspace just didn't work for me, don't know exactly why

**rush**

Too many config files

**nx**

Too complicated

**pnpm**

Simple config, simple usage, does only what is needed (creating symlinks for project/library interdependency)

# Community

### Roadmap

- [ ] My first goal is to write some scripts so you can pull one repo at a time so you dont have to pull the entire community at once, this wont be a problem now because this is new project with probably few submodules
- [ ] Make better usage of Lerna
- [ ] Integrate tools to track dependencies (maybe NX, maybe something else)
- [ ] Adopt best practices to avoid dependency hell

### Goals

- Help other devs to announce their projects
- Help other devs to find useful libraries and work with them
- Help other devs to structure their projects

### Principles (the usual)

- KISS
 Starting from bottom up and only implementing things one at a time and only after thorough planning
- YAGNI
 Avoiding burden of installation of things that are not required or needed
- DRY
 (Do I have to repeat it?)
