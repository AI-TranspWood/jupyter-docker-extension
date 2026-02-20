# Changelog

All notable changes to this project will be documented in this file.

## v1.0.3

- Add timeout to idle kernels to mitigate https://github.com/voila-dashboards/voila/issues/479

## v1.0.2

- Use `jupyter-server-proxy` to proxy the AiiDA REST API in the Jupyter environment instead of exposing an additional port.
  This allows users to access the REST API at `/proxy/5000` without needing to worry about port conflicts or security issues.

## v1.0.1

- Expose port 5000 for AiiDA REST API

## v1.0.0

- Initial release
