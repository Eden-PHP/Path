![logo](http://eden.openovate.com/assets/images/cloud-social.png) Eden Path
====
[![Build Status](https://api.travis-ci.org/Eden-PHP/Path.svg)](https://travis-ci.org/Eden-PHP/Path)
====

 - [Install](#install)
 - [Introduction](#intro)
 - [API](#api)
    - [absolute](#absolute)
    - [append](#append)
    - [getArray](#getArray)
    - [prepend](#prepend)
    - [pop](#pop)
    - [replace](#replace)
 - [Contributing](#contributing)

====

<a name="install"></a>
## Install

`composer install eden/path`

====

<a name="intro"></a>
## Introduction

Instantiate path in this manner.

```
$path = eden('path', '/some/path');
```

====

<a name="api"></a>
## API

==== 

<a name="absolute"></a>

### absolute

Attempts to get the full absolute path as described on the server. The path given must exist. 

#### Usage

```
eden('path', '/some/path')->absolute(string|null $root);
```

#### Parameters

 - `string|null $root` - The root path

Returns `Eden\Path\Index`

#### Example

```
eden('path', '/some/path')->absolute();
```

==== 

<a name="append"></a>

### append

Adds a path to the existing one 

#### Usage

```
eden('path', '/some/path')->append(*string $path);
```

#### Parameters

 - `*string $path` - The extra path to append

Returns `Eden\Path\Index`

#### Example

```
eden('path', '/some/path')->append('foo');
```

==== 

<a name="getArray"></a>

### getArray

Returns the path array 

#### Usage

```
eden('path', '/some/path')->getArray();
```

#### Parameters

Returns `array`

==== 

<a name="prepend"></a>

### prepend

Adds a path before the existing one 

#### Usage

```
eden('path', '/some/path')->prepend(*string $path);
```

#### Parameters

 - `*string $path` - The path to prepend

Returns `Eden\Path\Index`

#### Example

```
eden('path', '/some/path')->prepend('foo');
```

==== 

<a name="pop"></a>

### pop

Remove the last path 

#### Usage

```
eden('path', '/some/path')->pop();
```

#### Parameters

Returns `Eden\Path\Index`

==== 

<a name="replace"></a>

### replace

Replaces the last path with this one 

#### Usage

```
eden('path', '/some/path')->replace(*string $path);
```

#### Parameters

 - `*string $path` - replaces the last path with this

Returns `Eden\Path\Index`

#### Example

```
eden('path', '/some/path')->replace('foo');
```

==== 

<a name="contributing"></a>
#Contributing to Eden

Contributions to *Eden* are following the Github work flow. Please read up before contributing.

##Setting up your machine with the Eden repository and your fork

1. Fork the repository
2. Fire up your local terminal create a new branch from the `v4` branch of your 
fork with a branch name describing what your changes are. 
 Possible branch name types:
    - bugfix
    - feature
    - improvement
3. Make your changes. Always make sure to sign-off (-s) on all commits made (git commit -s -m "Commit message")

##Making pull requests

1. Please ensure to run `phpunit` before making a pull request.
2. Push your code to your remote forked version.
3. Go back to your forked version on GitHub and submit a pull request.
4. An Eden developer will review your code and merge it in when it has been classified as suitable.
