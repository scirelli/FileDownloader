Only tested in Chrome.

Requires the server to set a cookie (default in source is fileDownload=1).

//Example
(new scUtils.FileDownLoader(
    '../proxy/compress/compress.php?type=zip',
    {
        url:'www.yoursite.com'
    },
    'POST',
    //Error handler
    function( sStr ){
        //sStr is body content in the iframe, which is the output from the server.
        alert('some error' + sStr);
    }
) ).download();
