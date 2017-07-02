# Performance

## React Performance Tools

Use `react-addons-perf`

attach it to window and start it before mounting to root element.

```
window.Perf = Perf
Perf.start
```

browse app and then in console, stop the perf tools and view statistics

```
Perf.stop
Perf.printWasted()
```

If you have some components that are getting unnecessarily rendered, you can use `shouldComponentUpdate` to return false and tell react not to render it again. 

Note: adding of perf tools is for development only and must be removed before going to PROD.
