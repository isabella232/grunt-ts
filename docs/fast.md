# Fast compile configuration
Note : You must use *external modules* to be effective with `grunt-ts` fast compile.

Configuration is done via the `fast` *task* option. The following values are supported:

## watch
`watch`(default) which will clear the cache of the current target the first time it is called after `grunt-ts` has loaded (basically assumming that the js might have been out of date and just regenerating it *once*).
## always
`always` will *never* clear the cache (the `.tscache` folder) and it is up to the user to clear it (delete the `.tscache` folder)  if they purge the js. This is useful when you are using something like `webstorm` which always restarts `grunt-ts` and therefore we cannot take responsibility of clearing the cache for your. Use the option for `grunt-contrib-watch` as well.
## never
`never` Disables fast compile.
