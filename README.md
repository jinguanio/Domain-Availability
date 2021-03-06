Domain Availability Script
===================

[![Get help on Codementor](https://cdn.codementor.io/badges/get_help_github.svg)](https://www.codementor.io/helgesverre)

A PHP Class used to check if a domain has been registered.

Created to be fast and easy to use, modify and redistribute as you wish, credit me if appropriate.

## Install with Composer:
```
composer create-project -s dev cwd/domain-availability
```


## Install manually

1. Download the AvailabilityService.php file and place it "somewhere" in your project folder.
2. Include it in your PHP file.
3. Done.


## Usage:

```php
<?php
require('vendor/autoload.php');
$service = new HelgeSverre\DomainAvailability\AvailabilityService(true);

$available = $service->isAvailable("helgesverre.com");
if ($available) {
    echo $domain." is not registered\n";
} else {
    echo $domain." is registered\n";
}
```

or look at example.php for an example.

## Notes
The WHOIS server array is incomplete and some data is missing, the most popular TLD's are working though, I will update these as I can, I suggest making your own array of whois server information so you know which TLD is available, for a full list of TLD's and WHOIS servers please go to the [IANA website](http://www.iana.org/domains/root/db)

## Supported Domain Extensions
These are the domain extensions that are supported by this script.

``` 
.com, .net, .org, .co.uk, .io, .computer, .ac, .academy, .actor, .ae, .aero, .af, .ag, 
.agency, .ai, .am, .archi, .arpa, .as, .asia, .associates, .at, .au, .aw, .ax, .az, .bar, 
.bargains, .be, .berlin, .bg, .bi, .bike, .biz, .bj, .blackfriday, .bn, .boutique, .build, 
.builders, .bw, .by, .ca, .cab, .camera, .camp, .captial, .cards, .careers, .cat, .catering, 
.cc, .center, .ceo, .cf, .ch, .cheap, .christmas, .ci, .cl, .cleaning, .clothing, .club, 
.cn, .co, .codes, .coffee, .college, .cologne, .community, .company, .construction, 
.contractors, .cooking, .cool, .coop, .country, .cruises, .cx, .cz, .dating, .de, 
.democrat, .desi, .diamonds, .directory, .dk, .dm, .domains, .dz, .ec, .edu, .education,
.ee, .email, .engineering, .enterprises, .equipment, .es, .estate, .eu, .eus, .events,
.expert, .exposed, .farm, .feedback, .fi, .fish, .fishing, .flights, .florist, .fo, 
.foo, .foundation, .fr, .frogans, .futbol, .ga, .gal, .gd, .gg, .gi, .gift, .gl, .glass,
.gop, .gov, .graphics, .gripe, .gs, .guitars, .guru, .gy, .haus, .hk, .hn, .holiday, 
.horse, .house, .hr, .ht, .hu, .id, .ie, .il, .im, .immobilien, .in, .industries, 
.institute, .int, .international, .iq, .ir, .is, .it, .je, .jobs, .jp, .kaufen, .ke, 
.kg, .ki, .kitchen, .kiwi, .koeln, .kr, .kz, .la, .land, .lease, .li, .lighting, .limo, 
.link, .london, .lt, .lu, .luxury, .lv, .ly, .ma, .management, .mango, .marketing, .md,
.me, .media, .menu, .mg, .miami, .mk, .ml, .mn, .mo, .mobi, .moda, .monash, .mp, .ms,
.mu, .museum, .mx, .my, .na, .name, .nc, .nf, .ng, .ninja, .nl, .no, .nu, .nz, .om, 
.onl, .paris, .partners, .parts, .pe, .pf, .photo, .photography, .photos, .pics, 
.pictures, .pl, .plumbing, .pm, .post, .pr, .pro, .productions, .properties, .pt, 
.pub, .pw, .qa, .quebec, .re, .recipes, .reisen, .rentals, .repair, .report, .rest, 
.reviews, .rich, .ro, .rocks, .rodeo, .rs, .ru, .ruhr, .sa, .saarland, .sb, .sc, .se,
.services, .sexy, .sg, .sh, .shoes, .si, .singles, .sk, .sm, .sn, .so, .social, .solar, 
.solutions, .soy, .st, .su, .supplies, .supply, .support, .sx, .sy, .systems, .tattoo, 
.tc, .technology, .tel, .tf, .th, .tienda, .tips, .tk, .tl, .tm, .tn, .to, .today, 
.tools, .town, .toys, .tr, .training, .travel, .tv, .tw, .tz, .ua, .ug, .uk, .university, 
.us, .uy, .black, .blue, .info, .kim, .pink, .red, .shiksha, .uz, .vacations, .vc, .ve,
.vegas, .ventures, .vg, .viajes, .villas, .vision, .vodka, .voting, .voyage, .vu, .wang,
.watch, .wed, .wf, .wien, .wiki, .works, .ws, .xxx, .xyz, .yt, .zm, .zone, 
```

## Missing Domain Extensions

Due to the fact that a lot of the domain extentions listed on the IANA website, does not contain any information one which WHOIS server to use when querying for the domain information, the following domain extensions are not available (yet):

```
.dj, .do, .eg, .eh, .er, .et, .fj, .fk, .fm, .gallery, .gb, .ge, .gf, .gh, .gm, .gn, .gp,
.gq, .gr, .gt, .gu, .gw, .hm, .jetzt, .jm, .jo, .kh, .km, .kn, .kp, .kred, .kw, .ky, .lb, 
.lk, .lr, .ls, .mc, .mf, .mh, .mil, .mm, .moe, .mq, .mr, .mt, .mv, .mw, .mz, .nagoya, .ne, 
.neustar, .ni, .np, .nr, .nyc, .okinawa, .pa, .pg, .ph, .pk, .pn, .ps, .py, .qpon, .ren, 
.rw, .sd, .sj, .sl, .sohu, .sr, .ss, .sv, .sz, .td, .tg, .tj, .tokyo, .tp, .trade, .tt, 
.um, .uno, .va, .vi, .vi, .vn, .webcam, .ye, .yokohoma, .za, .ryukyu, .meet, .vote, .lc, 
.voto, .wed, .zw
```
If you know the whois server for any of these please feel free to create an issue with an update.


## Custom Integration Service!
If you need to integrate this script into your website, but don't have the knowledge to do so, I offer an integration service, email me at [email@helgesverre.com](mailto:email@helgesverre.com) (or use my [contact form](https://helgesverre.com/contact.php))  with a description of what you need to integrate with and I will give you a quote for my time.

I require 50% upfront payment for integration services.

## License

![Creative Commons](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)

This work is licensed under a Creative Commons Attribution-ShareAlike 4.0 International License.


Code and research by [Helge Sverre](https://helgesverre.com)
