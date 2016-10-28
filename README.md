# Deprecation warning

This project is deprecated in favour of [sallet](https://github.com/Fuco1/sallet).

# org-velocity

This is a "fork" of `org-velocity.el` from `org-contrib`.  To me, the original version behaves just plain insanely.  Maybe it tries to model itself after original, which is also insane, I don't know.  This fork fixes things that bothered me.  Here's a list

* Show the immediate header of the search, not the top-most level 1 header.  In the original, this resulted in one result for *whatever deep* subtree.  Insane.
* Don't show meta-bullshit after the header: properties, clocks, timers, logbooks...
* Unlinkify links: nothing better than seeing `[[file:~/download/02.%D0%A8%D0%BA%D0%B0%D1%82%D1%83%D0%BB%D0%BE%D1%87%D0%BA%D0%B0%20%D0%BF%D0%BE%D1%81%D0%BE%D0%B1%D0%B8%D0%B5%20%D0%BF%D0%BE%20%D1%87%D1%82%D0%B5%D0%BD%D0%B8%D1%8E%20%D0%B4%D0%BB%D1%8F%20%D0%B8%D0%BD%D0%BE%D1%81%D1%82%D1%80%D0%B0%D0%BD%D1%86%D0%B5%D0%B2,%20%D0%BD%D0%B0%D1%87%D0%B8%D0%BD%D0%B0%D1%8E%D1%89%D0%B8%D1%85%20%D0%B8%D0%B7%D1%83%D1%87%D0%B0%D1%82%D1%8C%20%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%B8%D0%B9%20%D1%8F%D0%B7%D1%8B%D0%BA%20(%D1%8D%D0%BB%D0%B5%D0%BC%D0%B5%D0%BD%D1%82%D0%B0%D1%80%D0%BD%D1%8B%D0%B9%20%D1%83%D1%80%D0%BE%D0%B2%D0%B5%D0%BD%D1%8C).pdf][reader]]`.  Just `(link):reader` would do (esp. as a quick search result)
* When there's just one result, follow it immediately (customizable)
* Don't visit results in indirect buffer (why the hell!).  Just pop to the buffer at the header containing result.  Even if plainly insane, I left the original behaviour as opt-in customize
* When the result is in a folded subtree, unfold the resulting header and its parents up to the level 1 header.
* Don't break window-configuration.  Whose brilliant idea was it to call `delete-other-windows`???
