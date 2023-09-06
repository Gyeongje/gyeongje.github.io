---
layout: page
title:  "Welcome to Pudhina"
subtitle: "A minimal Jekyll theme"
date:   2016-05-20 21:21:21 +0530
categories: ["general"]
---
You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

{% highlight python3 %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
# prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

{% highlight python %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
# prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

{% highlight C %}
int toupperw(int ch)
{
#if defined(_WIN_ALL)
  // CharUpper is more reliable than towupper in Windows, which seems to be
  // C locale dependent even in Unicode version. For example, towupper failed
  // to convert lowercase Russian characters.
  return (int)(INT_PTR)CharUpper((wchar *)(INT_PTR)ch);
#else
  return towupper(ch);
#endif
}
{% endhighlight %}

{% highlight c++ %}
int toupperw(int ch)
{
#if defined(_WIN_ALL)
  // CharUpper is more reliable than towupper in Windows, which seems to be
  // C locale dependent even in Unicode version. For example, towupper failed
  // to convert lowercase Russian characters.
  return (int)(INT_PTR)CharUpper((wchar *)(INT_PTR)ch);
#else
  return towupper(ch);
#endif
}
{% endhighlight %}

``` c++
int64 atoilw(const wchar *s)
{
  bool sign=false;
  if (*s=='-') // We do use signed integers here, for example, in GUI SFX.
  {
    s++;
    sign=true;
  }
  // Use unsigned type here, since long string can overflow the variable
  // and signed integer overflow is undefined behavior in C++.
  uint64 n=0;
  while (*s>='0' && *s<='9')
  {
    n=n*10+(*s-'0');
    s++;
  }
  // Check int64(n)>=0 to avoid the signed overflow with undefined behavior
  // when negating 0x8000000000000000.
  return sign && int64(n)>=0 ? -int64(n) : int64(n);
}
```

``` c
int64 atoilw(const wchar *s)
{
  bool sign=false;
  if (*s=='-') // We do use signed integers here, for example, in GUI SFX.
  {
    s++;
    sign=true;
  }
  // Use unsigned type here, since long string can overflow the variable
  // and signed integer overflow is undefined behavior in C++.
  uint64 n=0;
  while (*s>='0' && *s<='9')
  {
    n=n*10+(*s-'0');
    s++;
  }
  // Check int64(n)>=0 to avoid the signed overflow with undefined behavior
  // when negating 0x8000000000000000.
  return sign && int64(n)>=0 ? -int64(n) : int64(n);
}
```

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: http://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
