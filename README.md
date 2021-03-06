# `pitemp`

A quick and easy way to get the temperature of your Raspberry Pi with a single command. Built in [NodeJS](https://nodejs.org/en/).

![pitemp screenshot](https://i.imgur.com/gqvKva0.png)

## Usage

Requires [NodeJS](https://nodejs.org/en/).

### 1. Using `pitemp` with `npx`

The suggested usage is `npx`, because that way you'll always be running the latest version of `pitemp` without installing it. `npx` is installed by default with `npm`. You can get `npm` by installing [NodeJS](https://nodejs.org/en/).

```
npx pitemp

// pitemp is reporting every X seconds.
// Main: 62.322° C - Max: 62.322° C
```

### 2. Installing globally and running

You can install `pitemp` globally with your favorite package manager.

```
npm install -g pitemp
yarn global add pitemp
```

Then simply run `pitemp` with the command.

```
pitemp

// pitemp is reporting every X seconds.
// Main: 61.323° C - Max: 62.826° C
```

## Flags

### Time `-t <seconds>`

-   Default: `1`

Change the interval (in seconds) at which the temperature is reported.

### Verbose `-v`

Reports a more verbose log of your temperature.

#### Example using every flag:

```
npx pitemp -v -t 3
```

## Compatibility

| Machine                  | Operating System | Working |
| ------------------------ | ---------------- | ------- |
| Raspberry Pi 4 (4GB RAM) | Ubuntu 20.04     | Yes!    |
| MacBook Pro              | MacOS Catalina   | Yes!    |
| Windows (Intel)          | Windows 10       | Yes!    |

If you test this somewhere, please [create an issue](https://github.com/al5ina5/pitemp/issues/new) with your information on your machine and operating system so we can add it to this compatibility table.

## Troubleshooting

Try these steps _only after_ you've tried the package and received bad results.

### If you're on a Linux distro...

1. In some cases, you'll need to install the linux sensors package to be able to measure temperature. For example, on DEBIAN based systems, you can install them `sudo apt-get install lm-sensors`.

### If you're on Windows...

1. Ensure you're running `cmd` with administrator privileges.

### If you're on MacOS...

1. Ensure you've installed Xcode CLT, or force a fresh install by:
    1. Get the path of your current Xcode CLT. `xcode-select --print-path`
    2. Delete it. `sudo rm -r -f /Library/Developer/CommandLineTools`
    3. Install Xcode CLT. `xcode-select --install`

If you're still facing issues, [create an issue](https://github.com/al5ina5/pitemp/issues/new) and I'll try my best to help you out.
