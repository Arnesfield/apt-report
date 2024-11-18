# apt-report

Display list of packages grouped by apt repository using `apt policy` result.

Requires [Node.js](https://nodejs.org/).

## Install

1. Download `apt-report`.

   ```sh
   wget github.com/Arnesfield/apt-report/raw/main/apt-report -O apt-report
   ```

2. Make executable.

   ```sh
   chmod +x apt-report
   ```

3. Make sure `apt-report` is visible in `PATH`.

## Usage

Run the script:

```sh
apt-report
```

Can also accept `stdin`:

```sh
apt policy $(dpkg -l | awk 'NR >= 6 { print $2 }' | grep ^lib.*) | apt-report | less
```
