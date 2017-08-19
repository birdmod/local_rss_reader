# local_rss_reader

# Motivation
This project was done around may 2015 because I wanted to develop a local solution so a user could browse and manage 
its rss feeds over time without depending on a specific service. All in a single file for convenience so anyone could 
add it in favorites to use it. In fact, not everyone is a h4x0r. The audience can be your family or siblings that just use the browser to get info as they may not want to subscribe to a RSS service.

# Technologies
This project is a full client side HTML file with CSS and JavaScript.

# Challenges encountered
The biggest problem met was the fact that doing a request to a server from a AJAX call falls into the cross domain issue.
Basically we call from a *:file:///*...index.html a url hosted on http://*other-domain.com*/feed.
And this is not permitted. 
See the cross domain issue explained everywhere on the web.
But, the CORS technology allows it ... only if the server on which you query your feed supports it...

As I do not know which servers are going to be called by users and as I want a working project, I relied on Google Feed API ... which shut down in 2015 so I used the replacement found [here on rss2json](https://rss2json.com/)

# What does it look like ?
So this is a screenshot of the finished project that runs in the browser with already URLs stored and displaying articles
![Screenshot](screenshot_rss_reader.png?raw=true)
