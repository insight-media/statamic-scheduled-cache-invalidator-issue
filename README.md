## Issue
An exception is thrown when running "php artisan statamic:scheduled-cache-invalidator:run"

If a collection:
- has publish dates enabled
- is orderable

The NowScope will be applied, comparing the date on the 'order' field

## Steps to reproduce

- git clone insight-media/statamic-scheduled-cache-invalidator-issue
- composer install
- set STATAMIC_STATIC_CACHING_STRATEGY=half
- run "php artisan statamic:scheduled-cache-invalidator:run"
