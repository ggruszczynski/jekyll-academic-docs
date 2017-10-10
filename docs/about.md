## What Is Jekyll Academic
Jekyll Academic is a Jekyll template developed by NCSU Libraries tailored specifically for use within the academic community. It is a template for [Jekyll](https://jekyllrb.com/), a static website generator. It's features include the ability to create blog posts, a dedicated resume page, social media integration and the ability to create and host [Reveal.js](http://lab.hakim.se/reveal-js/#/) presentations. It is also designed to be hosted on GitHub pages. Jekyll Academic allows you to create a well designed, functional and completely free website. Hosting on GitHub pages allows you to keep the website in one place, even if you move between institutions.

## What is a Static Website?
Static websites are websites that do not require a database to store and deliver content to site visitors. In some ways static websites are more similar to early websites in that they rely primarily upon HTML and CSS to serve rather simple content to visitors. However, do not let the simplicity imply that they are somehow inferior to a dynamic website option such as WordPress.

Static websites have many advantages over dynamic websites. They are relatively simple to maintain, fast to load and incredibly secure. By creating a website that is not overly reliant upon third party software platforms you remain in total control of your content. You know exactly where every file for the website is, and do not have to worry about your content becoming trapped in a proprietary system or database.


## What is a Static Website Generator?
A static website generator is a tool that takes flat files and processes them into the necessary HTML and CSS files to become a website. In the case of Jekyll Academic the majority of the files are written using the Markdown markup language. It is a simplified text markup language that allows you to mimic the features of HTML without needing to know HTML. Jekll is built using the Ruby programming language, it can take the Markdown and sass files that are in the Jekyll Academic directory and process those files, creating a fully functioning website.

## Is This the Right Type of Site for Me?
While there are many advantages of using a static website generator to create your professional academic website, it may not be the right tool for everyone. This type of website is best suited for websites consisting mainly of static text content. If you need a site that relies heavily on video and large image galleries this may not be the best option for you. If you are looking for a site to host a CV and showcase some presentations as well as some text based pages (blog or otherwise) it will likely suit your needs.

## Testing Latex

Here is an example MathJax inline rendering \\( 1/x^{2} \\), and here is a block rendering: 
\\[ \frac{1}{n^{2}} \\]
  
 another \[x^{(n+1)} = x^{(n)} + p\]
 
 or
 
 
$$
\begin{align*}
  & \phi(x,y) = \phi \left(\sum_{i=1}^n x_ie_i, \sum_{j=1}^n y_je_j \right)
  = \sum_{i=1}^n \sum_{j=1}^n x_i y_j \phi(e_i, e_j) = \\
  & (x_1, \ldots, x_n) \left( \begin{array}{ccc}
      \phi(e_1, e_1) & \cdots & \phi(e_1, e_n) \\
      \vdots & \ddots & \vdots \\
      \phi(e_n, e_1) & \cdots & \phi(e_n, e_n)
    \end{array} \right)
  \left( \begin{array}{c}
      y_1 \\
      \vdots \\
      y_n
    \end{array} \right)
\end{align*}
$$
