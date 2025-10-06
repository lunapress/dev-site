# WordPress Dev Site

- PHP 8.3+

## Start

1. Clone the repository

   ```shell
   git clone git@github.com:onepix/wp-dev-site.git SITE.TEST
   ```

2. Install [DDEV](https://ddev.com/get-started/)

3. Rename `.ddev/config.override.yaml.example` to `.ddev/config.override.yaml`

4. Change in `.ddev/config.override.yaml` the `name`

5. Rename `.env.example` to `.env`

6. Rename `.ddev/docker-compose.mounts.yaml.example` to `.ddev/docker-compose.mounts.yaml` and write the path mapping with your plugins in the format `local:container`.

7. Install composer dependencies

   ```shell
   composer install
   ```

8. Launch the website

    ```shell
    ddev start
    ```


### ⚠️ Common issues

### Plugins not linking to the site (MacOS):  
Open `.ddev/mutagen/mutagen.yml`, remove the `#ddev-generated` line, add your plugin paths under `ignore.paths`, then run `ddev restart`.
