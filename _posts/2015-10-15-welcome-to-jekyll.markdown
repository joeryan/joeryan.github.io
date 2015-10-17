---
layout: post
title:  "My first experience with Jekyll!"
date:   2015-10-15 22:59:59
categories: jekyll update
---
This is just the first post and my first experience with jekyll.  I've had some  experience with Ruby and the Rails framework, but it's definitely been awhile.  I had the pleasure of attending the [Lansing Web MeetUp][Lansing-Web] just this past Wednesday, and got to hear some lightning talks about a number of static site generators in a couple of different languages.  I'll highlight them below more so that I won't forget them than that providing anyone else a great description.  But, maybe there will be some information that helps someone else out.

Dave Smith, from [Cognite labs][cognite], started things out with Jekyll which is based in Ruby.  Jekyll primarilly uses YAML for configuration, and can contain embedded Ruby code.  

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

It is actually the primary generator used in creating github pages.  Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll’s dedicated Help repository][jekyll-help].

Leo Dion, from [brightdigit][bright-digit] @brightdigit, showed us Metalsmith which uses JavaScript.  This scaffolding and uses YAML like jekyll, but the build scripts use either JS or json files - whichever you prefer.  It can use common plug ins for markdown, layouts, and permalinks.  He found it was more flexible and worked with Gulp, which was a consideration in his case.  The only down side is that there are sometimes EMCAScript6 and EMCAScript5 conflicts.

Dave Smith also presented Middleman, another generator writen in Ruby.  He was in the process of migrating many of [Cognite Labs][cognite] sites to use middleman.  It is faster than Jekyll and has access to all of ruby and rails.  The config.rb file can contain helper methods that are accessible through out the site.  It allows rapid switching between development and production environments.  It can also use code templates, following the DRY (don't repeat yourself) principle, and loop through a [data].yml file to display lists.  Another nice featuure is the ability to have sub-menus that can expand.  Unfortunately, the documentation leaves a lot to be desired.  It doesn’t push to github pages out of the box but ther are many other free or low cost places to publish static site content, such as [surge.sh][surge] and [netify.com][netify].  It can be hard to do images dynamically, but there is a gem that can do 3 versions of images.  It can use many other gems and the plugin eco sys is richer than jekyll's.  This is probably because it's easier to go build something for middleman than for Jekyll.

 Chris Fritz @chrisvfritz took on a quick overview of Hugo written in Go, since Patrick Hawkins couldn't be there.  Hugo build times are super fast compared to many other static site generators and uses all available cores on the system.  It also has rich plugin eco system, but for anything non-trivial you would need to know some Go.  On the plus side, Check out the youtube video [getting started with Go][get-go] for some good introductory information.  It compiles into executable code, but doesn’t feel like a low level language.

 Finally, Chris Fritz presented HJS-Webpack written in JavaScript.  This is basically webpack and react with the heavy lifting taken care of by HJS-webpack.  You do have to build everything from scratch and there is no cool plugin ecosystem and almost no docmentation.  But, you can build it all yourself! This ultimately gives you intimate knowledge of the generator.  You also get the full power of client side scripts but with selectable and customizable pre-rendering with no crazy Phantom-JS hacks.  It has live reloading with no state loss provided by the webpack development server and react live reload.  You can see the demo at [webpack-react.surge.sh][webpack-react] and get the source at [github.com/chrisvfritz/webpack-react-demo][webpack-react-demo].




[jekyll]: http://jekyllrb.com
[jekyll-gh]: https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
[Lansing-Web]: http://www.meetup.com/lansingweb/
[bright-digit]: http://www.brightdigit.com
[netify]: https://www.netlify.com
[surge]: http://surge.sh
[get-go]: https://www.youtube.com/watch?v=2KmHtgtEZ1s
[webpack-react]: http://webpack-react.surge.sh
[webpack-react-demo]: https://github.com/chrisvfritz/webpack-react-demo
[cognite]: http://www.cognitelabs.com
