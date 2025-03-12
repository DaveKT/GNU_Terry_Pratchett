# GNU_Terry_Pratchett

To add GNU Terry Pratchett to a write.as site, you need to include a custom HTTP header. Since write.as is a hosted platform with limited backend access, you can’t directly modify server settings. However, you can achieve the same effect using JavaScript.

## Steps

1.	Add a JavaScript snippet to your write.as site using the Custom JavaScript feature.
2.	Insert the following script in your site’s Customize section:

```
(function() {
    var meta = document.createElement('meta');
    meta.httpEquiv = "X-Clacks-Overhead";
    meta.content = "GNU Terry Pratchett";
    document.getElementsByTagName('head')[0].appendChild(meta);
})();
```


3.	Save the changes and test your site. While this won’t add a true HTTP header (since that requires server-side control), it ensures the message appears in the metadata of your page.

For the uninitiated, I first learned that this is all about, here: [https://mikecoats.com/x-clacks-overhead/](https://mikecoats.com/x-clacks-overhead/)
