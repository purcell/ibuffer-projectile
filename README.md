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

```el
(add-hook 'ibuffer-hook
    (lambda ()
      (ibuffer-projectile-set-filter-groups)
      (unless (eq ibuffer-sorting-mode 'alphabetic)
        (ibuffer-do-sort-by-alphabetic))))
```

Alternatively, use `ibuffer-projectile-generate-filter-groups'
to programmatically obtain a list of filter groups that you can
combine with your own custom groups.

To display filenames relative to the project root, use project-relative-file
in `ibuffer-formats`, e.g.:

```el
(setq ibuffer-formats
      '((mark modified read-only " "
              (name 18 18 :left :elide)
              " "
              (size 9 -1 :right)
              " "
              (mode 16 16 :left :elide)
              " "
              project-relative-file)))
```

I personally use [ibuffer-vc](https://github.com/purcell/ibuffer-vc)
because I prefer its grouping behaviour, but I thought this would be
useful to some people too.

## How to install ##

Add `ibuffer-projectile.el` to your `load-path`, or (preferred) install from [Melpa][Melpa].


[Melpa]: http://melpa.org "Melpa"

<hr>

[💝 Support this project and my other Open Source work](https://www.patreon.com/sanityinc)

[💼 LinkedIn profile](https://uk.linkedin.com/in/stevepurcell)

[✍ sanityinc.com](http://www.sanityinc.com/)
