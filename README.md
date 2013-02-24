# Google Reader API client  ( roodo version )

#### This is a Google Reader API client in Ruby.

  This forked version provides extra abilities to:

     1. Subscribe to a particular feed.

     2. Unsubscribe a particular feed.

     3. Retrieves unread entries.

     4. Mark unread entries as read.

  Usage: First you can use omniauth-google-oauth2 gem to get Google OAuth2 access token.

     client =  GReader.auth :email => 'email@abc.com', :access_token => OAuth2_token

     1. Subscribe to a particular feed.

            client.subscribe( feed_url )

     2. Unsubscribe a particular feed.

            client.unsubscribe( feed_url )

     3. Retrieves unread entries.

            unread_entries = client.unread_list( limit = 20 )

     4. Mark unread entry as read.

            entry = unread_entries.first

            entry.mark_read


  Debug in rails console (to see the details of API requests made by RestClient):

     RestClient.log = "stdout"


### Authors

 * Edward, roodo inc.  [ netloner@gmail.com ]

The original version is authored and maintained by Rico Sta. Cruz (github.com/rstacruz),
with contributions from:

 * Colin Gemmell (pythonandchips.net)
