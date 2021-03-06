# js-style-guides
This Repo provides a simple JS Style Guides.

## Installation

### Step 1
```bash
sudo npm install --global babel-eslint eslint-plugin-react eslint esformatter esformatter-add-trailing-commas esformatter-quote-props esformatter-semicolons esformatter-spaced-lined-comment
```

### Step 2
Download this repo, unzip the `js-style-guides-master` folder in the same level of your Project's folder.

### Step 3
Enter to the `js-style-guides-master` folder and modify the paths included in the `.eslintignore` file, it should point to your Project's folder

## Configuration

### Atom

#### Go to Atom Menu > Preferences > Install
Search and Install the packages: `linter` and `linter-eslint`.

#### Enter to the `linter-eslint`' settings

<img src="https://github.com/StevenPerez/images/blob/master/atom-lint-settings.png?raw=true"></img>

### WebStorm

<img src="https://github.com/StevenPerez/images/blob/master/webstorm-eslint-settings.png?raw=true"></img>

### Sublime Text

#### Way #1:

#### Install the `ESlint` and `SublimeLinter-contrib-eslint` packages.

#### Go to Sublime Text Menu > Preferences > Package Settings > ESlint > Settings Default

Copy the following JSON config:

```bash
{
  "node_path": "/usr/local/bin",
  "node_modules_path": "/usr/local/lib/node_modules",
  "config_file": "<FULLPATH>/js-style-guides-master/.eslintrc"
}

```

#### Way #2:

#### Install the `ESlint`, `SublimeLinter`, `SublimeLinter-contrib-eslint` and `SublimeLinter-contrib-eslint_d` packages.

#### Go to Sublime Text Menu > Preferences > Package Settings > SublimeLinter > Settings Default

Update the `linters` property according to the following JSON config:

```bash
"linters": {
    "eslint": {
        "@disable": false,
        "args": [
            "--rulesdir",
            "<FULLPATH>/js-style-guides-master",
            "--ignore-path",
            "<FULLPATH>/js-style-guides-master/.eslintignore",
            "-c",
            "<FULLPATH>/js-style-guides-master/.eslintrc"
        ],
        "excludes": []
    },
    "eslint_d": {
        "@disable": false,
        "args": [],
        "excludes": []
    }
}
```


