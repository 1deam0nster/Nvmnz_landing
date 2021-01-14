# Rin 5 + bulma

A lean HTML & SASS boilerplate for better front-end coding

<https://sanographix.github.io/rin/>
<https://bulma.io>

# Getting Started

### Required Components

- Node.js
    - <http://nodejs.org/>

## Set Up

#### 1) Clone Rin:

    $ git clone git@github.com:surepu/starter.git starter
    $ cd starter
    $ npm install

#### 3) Run rin:

    $ npm start

#### 4) :tada:

<hr/>

# Directory

While you are running Rin, It is watching directories under `src/`. Put your project’s templates(ejs), scss, js, images files in it.

`templates/`, `scss/`, `js/`, `images/` files will compile and output to `build/`.

	rin/
	┣┳ src/
	┃┣ templates/
	┃┣ scss/
	┃┣ js/
	┃┗ images/
	┃
	┗┳ build/
	 ┗┳ index.html
	  ┣ css/
	  ┣ js/
	  ┗ images/

# Templates

Rin supports [EJS](http://www.embeddedjs.com/) template. When you edit and save `.ejs` files under `src/templates/pages`, they will output as `.html` to `build/` directory.

## Template tags

### site.json

Put variables which use for every pages.

Example:

	{
	  "siteName": "Example Site",
      "siteRootUrl": "http://example.com/",
      "ogImageUrl": "http://example.com/images/og-image.jpg",
      "fbAppId": "000000000",
      "twitterSite": "@sanographix",
      "googleAnalyticsId": "UA-00000000-1"
	}

### index.ejs

To use variables for particular single page, put variables into `<% var %>` at each page.

#### Example:

	<% var
	pageTitle = "Toppage";
	pageDescription = "Example site";
	%>
	<head>
		<title><%= pageTitle %> - <%= siteName %></title>
		<meta property="og:description" content="<%= pageDescription %>" />
	</head>

#### Result:

	<head>
		<title>Toppage - Example Site</title>
		<meta property="og:description" content="Example site" />
	</head>

# Images

Rin optimizes gif, jpg, png, svg images automatically using [imagemin](https://www.npmjs.com/package/imagemin-cli). Each files will output to `build/images/`.

# CSS

Rin supports scss.

	sсss
	┣ style.scss // It imports under /lib files
  ┣ custom.scss // styles for all pages
	┗ pages 

# JS

js files under `src/js/` will output to `build/js/scripts.js` with concatenated and compressed.

# Local Server

Rin runs local server by using [BrowserSync](https://www.browsersync.io/). Its default URL is <http://localhost:3000/>. It reloads your browser automatically when you update a file.

# Deploy to gh-pages branch

Run `git subtree` command.

```
git subtree push --prefix build/ origin gh-pages
```
- [Deploy to `gh-pages` from a `dist` folder on the master branch. Useful for use with yeoman](https://gist.github.com/cobyism/4730490)

# Author

### Showkaku Sano (sanographix)

Graphic designer from Kyoto.

- <https://sanographix.net/>
- Twitter: [@sanographix](https://twitter.com/sanographix/)

# License

MIT
# nvmnz
