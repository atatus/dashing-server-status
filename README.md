## Server Status widget to Dashing

**Kudos to [willjohnson](https://gist.github.com/willjohnson/6313986)**

This is a [Dashing](http://shopify.github.com/dashing) widget to checks whether a server is responding to either an `http` or `ping` request. It displays either a check or alert depending on the response.

![](https://raw.githubusercontent.com/atatus/dashing-server-status/master/preview.png)

## Usage

1. Copy `server_status.coffee`, `server_status.html`, and `server_status.scss` into the `/widgets/server_status` directory of your Dashing app.

2. Copy the `server_status.rb` file into your `/jobs` folder.

3. In the `server_status.rb`, update your server information

```
servers = [{name: 'server1', url: 'https://www.test.com', method: 'http'},
        {name: 'server2', url: 'https://www.test2.com', method: 'http'},
        {name: 'server3', url: '192.168.0.1', method: 'ping'}]
```

To include the widget in a dashboard, add the following snippet to the dashboard layout file:

```html
<li data-row="1" data-col="1" data-sizex="1" data-sizey="1">
    <div data-id="server_status" data-view="ServerStatus" data-title="Server Status"></div>
</li>
```

