# MD Cloud Integration

This script provides command-line tools for MD Cloud Integration, including authentication and uploading cases.

## Requirements

- Python 3.x
- Required environment variables:
  - `PSR_CLOUD_USER`
  - `PSR_CLOUD_PASSWORD_HASH`
  - `PSR_CLOUD_CONSOLE_PATH`

## Installation

1. Clone the repository:
   ```sh
   git clone https://your-repo-url.git
   cd your-repo-directory
   ```

2. Install the required dependencies:
   ```sh
   pip install -r requirements.txt
   ```

## Usage

### General Usage

To see the available commands and options, run:
```sh
.\dist\mdcloudintegration.exe --help
```

### Authentication

To authenticate with the MD Cloud, use the `auth` command:
```sh
.\dist\mdcloudintegration.exe auth
```

### Upload Case

To upload a case, use the `upload` command with the required arguments:
```sh
.\dist\mdcloudintegration.exe upload --casepath <path_to_case> --casename <case_name> [--cluster <cluster_name>]
```

#### Example

```sh
.\dist\mdcloudintegration.exe upload --casepath D:\Bitbucket\pycloud\tests\cases\example --casename example_case --cluster PSR-US_STAGING
```

## Arguments

- `--version`: Show the version of the MD Cloud Integration tool.
- `auth`: Authenticate with the MD Cloud.
- `upload`: Upload a case to the MD Cloud.
  - `--casepath`: (Required) The path to the case directory.
  - `--casename`: (Required) The name of the case.
  - `--cluster`: (Optional) The name of the cluster to upload the case to.

## Environment Variables

Ensure the following environment variables are set before running the script:

- `PSR_CLOUD_USER`: Your MD Cloud username.
- `PSR_CLOUD_PASSWORD_HASH`: The hash of your MD Cloud password.
- `PSR_CLOUD_CONSOLE_PATH`: The path to the MD Cloud console.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.