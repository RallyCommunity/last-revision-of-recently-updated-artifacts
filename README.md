Last revision of recently updated artifacts
=========================

## Overview
![](pic0.png)
Getting and parsing revision history is expensive. To make this more efficient and performant the artifacts are queried by LastUpdateDate which is hardcoded to go back two days from the current date:
```
var startDate = new Date(new Date() - 86400000*2).toISOString(); //in the last 2 days; millisecondsInDay = 86400000
        
        var filters = [
            {
                property : 'LastUpdateDate',
                operator : '>=',
                value : startDate
            }	
   	];
```
This app is vailable AS IS. It is NOT supported by Rally.
## License

AppTemplate is released under the MIT license.  See the file [LICENSE](./LICENSE) for the full text.

##Documentation for SDK

You can find the documentation on our help [site.](https://help.rallydev.com/apps/2.0rc2/doc/)
