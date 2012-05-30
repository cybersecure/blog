CyberSecure blog
================

This is the source of the cybersecure blog.

STRUCTURE
---------

* This repositry has two branches: master & gh-pages
  
  * **master** - Make all the changes here, this should reflect any drafts or changes to style we need to make.
  * **gh-pages** - This is the published branch of the repo. Anything that is pushed to this branch on github will be published to the live site.

* All the posts are located under _posts folder. Each individual file is a post in itself.
  
  * Post file needs the following parts
    <pre><code>
    ---
    layout: post
    title: title of the post
    ---

    p(meta). date of the publication - place of the publication ( this part is optional )
    </code></pre>
  * Each post file is named in the following pattern:
    <code>year-month-date-title-of-the-post.textile</code>
  * All the content is written in textile markup. Please read about it before writing a post.

* All the changes can be seen live on the development machine by following this procedure.

  * Make the changes and start the server by running <code>foreman start</code>
  * Visit the webpage on port 4000 on the local machine.

HOW TO PUBLISH
--------------

Follow these steps to publish a new post:

* Checkout branch master : <code>git checkout master</code>
* Make a copy of one of the previous posts.
* Change the name in the post pattern : <code>year-month-date-title-of-the-post.textile</code>
* Change the title and the meta information for the post.
* Write the post in textile markup and save the file.
* Preview the changes by running the dev server <code>foreman start</code> and visiting <code>http://storage1:4000</code>.
* Add the new file to git. <code>git add .</git>
* Commit the changes to git <code>git commit</code>
* Push the changes to github <code>git push origin master</code>
* Checkout branch gh-pages : <code>git checkout gh-pages</code>
* Merge the master branch into the gh-pages branch <code>git merge master</code>
* Push the changes to github <code>git push origin gh-pages</code>
