# mathoid

Vagrant machine to configure an Ubuntu Trusty 14.04 64-bit box with Mathoid based on Node.js & Phantomjs Chef Solo scripts. Based on steps here: [http://www.formulasearchengine.com/mathoid](http://www.formulasearchengine.com/mathoid).

## Install Vagrant & VirtualBox

### Install Vagrant 1.5+

[http://vagrantup.com](http://vagrantup.com)

__Note: you need 1.5 or newer for boxes to automatically download and install.__

### Install VirtualBox

[https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)

## Provision a VM

```
git clone git@github.com:cbumgard/mathoid-vagrant.git
cd mathoid-vagrant
git submodule init
git submodule update
vagrant up
vagrant ssh
```

## Test: CLI

From either the host or the guest you should now be able to run:

```
curl -d 'q=E=mc^2' localhost:10042
```

And get the response:

```
{
  "input":"E=mc^2",
  "svg":"<svg xmlns:xlink=\"http://www.w3.org/1999/xlink\" style=\"width: 9ex; height: 2.111ex; vertical-align: -0.222ex; margin-top: 1px; margin-right: 0px; margin-bottom: 1px; margin-left: 0px; position: static; \" viewBox=\"0 -861.7994854101626 3885.6444800547624 904.702786738219\" xmlns=\"http://www.w3.org/2000/svg\"><defs id=\"MathJax_SVG_glyphs\"><path id=\"MJMATHI-45\" stroke-width=\"10\" d=\"M492 213Q472 213 472 226Q472 230 477 250T482 285Q482 316 461 323T364 330H312Q311 328 277 192T243 52Q243 48 254 48T334 46Q428 46 458 48T518 61Q567 77 599 117T670 248Q680 270 683 272Q690 274 698 274Q718 274 718 261Q613 7 608 2Q605 0 322 0H133Q31 0 31 11Q31 13 34 25Q38 41 42 43T65 46Q92 46 125 49Q139 52 144 61Q146 66 215 342T285 622Q285 629 281 629Q273 632 228 634H197Q191 640 191 642T193 659Q197 676 203 680H757Q764 676 764 669Q764 664 751 557T737 447Q735 440 717 440H705Q698 445 698 453L701 476Q704 500 704 528Q704 558 697 578T678 609T643 625T596 632T532 634H485Q397 633 392 631Q388 629 386 622Q385 619 355 499T324 377Q347 376 372 376H398Q464 376 489 391T534 472Q538 488 540 490T557 493Q562 493 565 493T570 492T572 491T574 487T577 483L544 351Q511 218 508 216Q505 213 492 213Z\"></path><path id=\"MJMAIN-3D\" stroke-width=\"10\" d=\"M56 347Q56 360 70 367H707Q722 359 722 347Q722 336 708 328L390 327H72Q56 332 56 347ZM56 153Q56 168 72 173H708Q722 163 722 153Q722 140 707 133H70Q56 140 56 153Z\"></path><path id=\"MJMATHI-6D\" stroke-width=\"10\" d=\"M21 287Q22 293 24 303T36 341T56 388T88 425T132 442T175 435T205 417T221 395T229 376L231 369Q231 367 232 367L243 378Q303 442 384 442Q401 442 415 440T441 433T460 423T475 411T485 398T493 385T497 373T500 364T502 357L510 367Q573 442 659 442Q713 442 746 415T780 336Q780 285 742 178T704 50Q705 36 709 31T724 26Q752 26 776 56T815 138Q818 149 821 151T837 153Q857 153 857 145Q857 144 853 130Q845 101 831 73T785 17T716 -10Q669 -10 648 17T627 73Q627 92 663 193T700 345Q700 404 656 404H651Q565 404 506 303L499 291L466 157Q433 26 428 16Q415 -11 385 -11Q372 -11 364 -4T353 8T350 18Q350 29 384 161L420 307Q423 322 423 345Q423 404 379 404H374Q288 404 229 303L222 291L189 157Q156 26 151 16Q138 -11 108 -11Q95 -11 87 -5T76 7T74 17Q74 30 112 181Q151 335 151 342Q154 357 154 369Q154 405 129 405Q107 405 92 377T69 316T57 280Q55 278 41 278H27Q21 284 21 287Z\"></path><path id=\"MJMATHI-63\" stroke-width=\"10\" d=\"M34 159Q34 268 120 355T306 442Q362 442 394 418T427 355Q427 326 408 306T360 285Q341 285 330 295T319 325T330 359T352 380T366 386H367Q367 388 361 392T340 400T306 404Q276 404 249 390Q228 381 206 359Q162 315 142 235T121 119Q121 73 147 50Q169 26 205 26H209Q321 26 394 111Q403 121 406 121Q410 121 419 112T429 98T420 83T391 55T346 25T282 0T202 -11Q127 -11 81 37T34 159Z\"></path><path id=\"MJMAIN-32\" stroke-width=\"10\" d=\"M109 429Q82 429 66 447T50 491Q50 562 103 614T235 666Q326 666 387 610T449 465Q449 422 429 383T381 315T301 241Q265 210 201 149L142 93L218 92Q375 92 385 97Q392 99 409 186V189H449V186Q448 183 436 95T421 3V0H50V19V31Q50 38 56 46T86 81Q115 113 136 137Q145 147 170 174T204 211T233 244T261 278T284 308T305 340T320 369T333 401T340 431T343 464Q343 527 309 573T212 619Q179 619 154 602T119 569T109 550Q109 549 114 549Q132 549 151 535T170 489Q170 464 154 447T109 429Z\"></path></defs><g stroke=\"black\" fill=\"black\" stroke-width=\"0\" transform=\"matrix(1 0 0 -1 0 0)\"><use href=\"#MJMATHI-45\" xlink:href=\"#MJMATHI-45\"></use><use href=\"#MJMAIN-3D\" x=\"1046\" y=\"0\" xlink:href=\"#MJMAIN-3D\"></use><use href=\"#MJMATHI-6D\" x=\"2107\" y=\"0\" xlink:href=\"#MJMATHI-6D\"></use><g transform=\"translate(2990,0)\"><use href=\"#MJMATHI-63\" xlink:href=\"#MJMATHI-63\"></use><use transform=\"scale(0.7071067811865476)\" href=\"#MJMAIN-32\" x=\"619\" y=\"513\" xlink:href=\"#MJMAIN-32\"></use></g></g></svg>",
  "mml":"<math xmlns=\"http://www.w3.org/1998/Math/MathML\">\n  <semantics>\n    <mrow>\n      <mi>E</mi>\n      <mo>=</mo>\n      <mi>m</mi>\n      <msup>\n        <mi>c</mi>\n        <mn>2</mn>\n      </msup>\n    </mrow>\n    <annotation encoding=\"application/x-tex\">E=mc^2</annotation>\n  </semantics>\n</math>",
  "log":"0: E=mc^2.. 6B query, OK 3666B result, took 11ms.",
  "success":true
}
```

## Test: Browser

Navigate to [http://localhost:10042/](http://localhost:10042/). You should see:

![Screenshot](https://i.cloudup.com/PAh_mz8ad3.png)

## Troubleshooting

If for some reason Vagrant cannot find the precise64 base box manually install it via:

```
vagrant box add hashicorp/precise64
```
