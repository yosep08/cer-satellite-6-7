
# Styles for CER

The following styles or themes are available for CER.
*Excluding* the specific fonts for these languages and locale.

The styles can be found under `pdf/styles`:

* redhat-theme.yml
* redhat-zh_CN-theme.yml
* redhat-ja_JP-theme.yml
* redhat-ko_KR-theme.yml
* redhat-zh_TW-theme.yml

To change the current style in use.
A change must be made in file `vars/render-vars.adoc`.

Change the line containing `:pdf-style: redhat` into:

* `:pdf-style: redhat-zh_CN`
* `:pdf-style: redhat-ja_JP`
* `:pdf-style: redhat-ko_KR`
* `:pdf-style: redhat-zh_TW`

The needed fonts have to be placed in `fonts/` directory.
And can be found at `https://gitlab.consulting.redhat.com/kmo-consulting-engagement-reports/cer-tools/cer-styling/-/tree/master/fonts`.

Until we have an automated way of copying the fonts you have to manually copy the needed fonts.




