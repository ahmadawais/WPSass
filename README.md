<table width="100%">
    <tr>
        <td align="left" width="100%" colspan="2">
            <strong>WPSass</strong><br />
            Use Sass with WordPress via NPM Scripts.
        </td>
    </tr>
    <tr>
        <td>
            A FOSS (Free & Open Source Software) project. Maintained by <a href="https://github.com/ahmadawais">@AhmadAwais</a>.
        </td>
        <td align="center">
            <a href="https://AhmadAwais.com/">
                <img src="https://i.imgur.com/Asg4d3k.png" width="100" />
            </a>
        </td>
    </tr>
</table>

Use Sass with WordPress, Node Script in SCSS flavor.

# 🎗 WP Sass — Getting Set up

Make sure you have node installed. If not [download and install node](https://nodejs.org/en/download/).

## → STEP #1: Install NodeJS & NPM
After installing NodeJS you can verify the install of both NodeJS and Node Package Manager by typing the following commands. This step needs to be followed only once i.e. if you don't have NodeJS installed. No need to repeat it ever again.

```bash
node -v
# v7.10.0

npm -v
# 4.2.0
```

## → Step #2. Download `package.json`

Download [`package.json`](https://git.io/vHLHg) file inside the root folder of your WordPress plugin or WordPress theme
If you have cURL installed then you can run the following command to download it in one go (just make sure you open the root folder of your WordPress plugin or WordPress theme and download [`package.json`](https://git.io/vHLHg) file in it).

```bash
curl -L 'https://git.io/wpsass' -o package.json
```

## → STEP #3: Installing Node Dependencies

We are in the root folder of our WordPress plugin or WordPress theme at the moment, let's install the Node Dependencies. In the terminal run this command and wait for it to download all the NodeJS dependencies. It's a one time process and can take about a minute depending on the internet speed of your connection.

```bash
# For MAC OS X run the following command with super user
sudo npm install

# For Linux run the following command
npm install
```

## → STEP #4: Configure NPM Scripts

Now, configure the NPM scripts. There are only two of them. If you open the [`package.json`](https://git.io/vHLHg) file. There are two scripts as follows:

```json
"scripts": {
  "css": "node-sass --output-style compressed --include-path scss assets/css/source.scss style.css",
  "watch": "nodemon -e scss -x \"npm run css\""
},
```

In the `css` script, you need to change
- SCSS Source File Path & Name — `assets/css/source.scss`
- Destination CSS File Path & Name — `style.css`

> NOTE: That currently this little app has following file structure
```bash
    ├── assets
    |  └── css
    |     ├── partial
    |     |  ├── base.scss
    |     |  └── variables.scss
    |     ├── source.scss
    |     └── vendor
    |        └── normalize.css
    ├── index.html
    ├── package.json
    └── style.css
```

`source.scss` is the source file for SCSS files, which imports files from `partials` and `vendor` directory. This gets compiled into a `style.css` file in the root of our project as configured in the npm script.


## → STEP #5: Run NPM Scripts

All that's left now is for you to run the NPM script in the root folder of your WP project — where you downloaded the [`package.json`](https://git.io/vHLHg) file.

> NOTE: Before you run, make sure there is a source SCSS file. Otherwise running the script will display this error `An output directory must be specified when compiling a directory`.

```bash
# Compile CSS.
npm run css
```

```bash
# Watch changes in SCSS files and compile CSS automatically.
npm run watch
```


## → STEP #6: Share!

Yup, there are no more steps. Just share it with your friends. Or [Click to Tweet about it](https://twitter.com/home?status=%F0%9F%94%A5%20WPSass%3A%20A%20neat%20little%20pkg%20by%20%40MrAhmadAwais%20to%20compile%20%26%20watch%20Sass%20SCSS%20to%20CSS%20via%20NPM%20Scripts%20%E2%80%94%20take%20a%20look%20%E2%86%92%20ahmda.ws/to_WPS).

## Contribute
Feel free to contribute. PR's are welcomed.

## Changelog

### Version 1.0.0 
- First version
- Compile: SCSS to CSS
- Watch: Changes in SCSS


## License
Released under MIT License.
Copyright [Ahmad Awais](https://AhmadAwais.com/)

---

🙌 — If 500 people [signup here](http://eepurl.com/cLwjeH), I will build a video series for this.
