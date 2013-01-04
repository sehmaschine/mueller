MUELLER
=======

**Modular Grid System**.

About
=====

MUELLER is a modular grid system for responsive/adaptive and non-responsive layouts, based on `Compass <http://compass-style.org/>`_.
You have full control over column width, gutter width, baseline grid and media-queries.

Modules
=======

Media
-----

One default grid and (if needed) different per-media grids (e.g. large, tablet, handheld)::

    @include grids(d,
        24,
        20px,
        20px,
        0 2 3 4 6 8 12 16 24,
        0 2 4 6 8 12);

Layouts
-------

Extend your media-grids to pre-defined layouts (e.g. a 2-column layout with switched columns)::

    .l-2c {
        @extend .g-d-24;
        @extend .g-l-24;
        @extend .g-tp-12;
        @extend .g-h-6;
        .c-1 {
            @extend .g-d-12;
            @extend .g-l-12;
            @extend .g-tp-6;
            @extend .g-h-3;
        }
        .c-2 {
            @extend .g-d-12;
            @extend .g-l-12;
            @extend .g-tp-6;
            @extend .g-h-3;
        }
    }

Fractions
---------

On top of grids and layouts, add fractional classes (e.g. all-half, all-thirds, all-1of3)::

    .g-all-half {
        .l-1c .c-1 & {
            @extend .g-d-12;
            @extend .g-l-12;
            @extend .g-tp-6;
            @extend .g-h-3;
        }
    }

Templates
---------

The semantic way &mdash; add templates instead of using presentational classes in your markup::

    .template-1 {
        #page {
            @extend .l-2c;
        }
        #content {
            @extend .c-1;
        }
        #sidebar {
            @extend .c-2;
        }
    }

Examples
========

see index.html and `www.muellergridsystem.com <http://www.muellergridsystem.com>`_.


Practice
========

MUELLER is NOT working out of the box.
Read the Code, read `this <http://chriseppstein.github.com/blog/2011/08/21/responsive-layouts-with-sass/>`_ and try to understand what´s happening.
Learn `Sass <http://sass-lang.com/>`_/`Compass <http://compass-style.org/>`_.

Change the grid, change the baseline, activate/deactivate different media-queries, add layouts/fractions.
Figure out what´s working best for you.

Think about your layout first &mdash; you can´t just add "responsiveness" to every given layout.
Reflect on `Mobile First <http://www.abookapart.com/products/mobile-first>`_, use `HTML5 <http://html5doctor.com/>`_.

System
======

You mainly get the file grid_system – this is where the system is defined.
All other parts (media, layouts, fractions, templates) are just examples of how to work with MUELLER.
MUELLER is licensed under `BSD <http://opensource.org/licenses/BSD-3-Clause>`_.

Credits
=======

MUELLER is largely a copy of the ideas outlined by `Chris Eppstein <http://chriseppstein.github.com/blog/2011/08/21/responsive-layouts-with-sass/>`_ and heavily inspired by the work of `Joni Korpi <http://jonikorpi.com/>`_.
The name MUELLER refers to `Josef Müller-Brockmann <http://en.wikipedia.org/wiki/Josef_M%C3%BCller-Brockmann>`_. Besides, it´s part of my last name.