# About this repo

This repo is the source for http://borderlandsmodding.com/

Editing should be pretty straightforward:

- The links at the top of the page, and on the sidebar, are
  defined in `_data/navigation.yml`
- The links at the bottom of the page are defined in `_config.yml`
- Pages are in `_pages`; just follow how the other ones
  look.  Be sure to put a `permalink` up in the top like
  all the other current pages do
- Blog-like posts are kept in `_posts` - stick to the naming
  convention in there of `YYYY-MM-DD-title.md`, and be sure to
  include a top-level heading (using markdown's `#`).
- The site uses the repo BLCM/modding-web-theme for its Jekyll
  theme (which is the thing Github Pages uses to generate the
  site).  If you were looking to change something cosmetic on
  the site, that'd be the place to do it.  Note that if you
  change something in the theme, you'll have to then make another
  commit in this repo in order to pick up the change; it won't
  automatically apply to the site if *just* the theme is
  updated.

**Note:** After you've pushed a change here, it will be a few
tens of seconds before the "live" page is updated, so be patient.
Be careful when editing any of the `*.yml` files; if you screw
those up, changes will stop showing up on the main site.  So if
you're editing those and nothing's changed after 30 seconds or
so, you may want to revert your changes.

I'd personally intend for the blog-like posts to be primarily
about more major things that happen, rather than trying to detail
every little thing.  New releases of UCP or BLCMM should be
mentioned in there, for instance, and "exciting" things like
Borderlands Commander which open up new avenues of modding.  The
recent chaos with the BL2+TPS UHD packs would be another good
example of a case where a post might be a good idea, just to
have a summary URL to point users to.
