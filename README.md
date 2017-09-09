[![Melpa Status](http://melpa.org/packages/ibuffer-projectile-badge.svg)](http://melpa.org/#/ibuffer-projectile)
[![Melpa Stable Status](http://stable.melpa.org/packages/ibuffer-projectile-badge.svg)](http://stable.melpa.org/#/ibuffer-projectile)
<a href="https://www.patreon.com/sanityinc"><img alt="Support me" src="https://img.shields.io/badge/Support%20Me-%F0%9F%92%97-ff69b4.svg"></a>

# ibuffer-projectile: Group buffers in ibuffer list by projectile project #

Emacs' `ibuffer-mode` is a wonderful replacement for the built-in
`list-buffer` command, and allows buffers to be grouped
programatically, e.g. by major mode.

`ibuffer-projectile` lets you group your buffers by their projectile
root directory.

You can use this package manually or automatically. For manual use,
call `ibuffer-projectile-set-filter-groups`. To have this function
called when you open ibuffer, add this hook to your configuration:

```
(add-hook 'ibuffer-hook
    (lambda ()
      (ibuffer-projectile-set-filter-groups)
      (unless (eq ibuffer-sorting-mode 'alphabetic)
        (ibuffer-do-sort-by-alphabetic))))
```

Alternatively, use `ibuffer-projectile-generate-filter-groups'
to programmatically obtain a list of filter groups that you can
combine with your own custom groups.

I personally use [ibuffer-vc](https://github.com/purcell/ibuffer-vc)
because I prefer its grouping behaviour, but I thought this would be
useful to some people too.

## How to install ##

Add `ibuffer-projectile.el` to your `load-path`, or (preferred) install from [Melpa][Melpa].


[Melpa]: http://melpa.org "Melpa"

<hr>

[![](http://api.coderwall.com/purcell/endorsecount.png)](http://coderwall.com/purcell)

[![](http://www.linkedin.com/img/webpromo/btn_liprofile_blue_80x15.png)](http://uk.linkedin.com/in/stevepurcell)

[Steve Purcell's blog](http://www.sanityinc.com/) // [@sanityinc on Twitter](https://twitter.com/sanityinc)
