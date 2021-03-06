+++
title = "Language Configuration"
description = "Configuring the default language option for your BookStack instance"
date = "2018-08-11"
type = "admin-doc"
+++

By default the BookStack interface is shown in English. Additional languages are supported
by the wider BookStack community. English translations may show as a fallback if a chosen
alternative language does not have fully up-to-date translations.  

### Setting the Default Language

The value of the `APP_LANG` variable needs to be a valid locale code
The default language will be used as the default for logged-in users and also for
public users if their language cannot be auto-detected. This can be set
 in your `.env` file as follows:

```bash
# Sets application language to French
APP_LANG=fr
```

The value of the `APP_LANG` variable must be a valid locale code matching one of the following options:

* English - `en`
* German - `de`
* Spanish - `es`
* Spanish, Argentinian - `es_AR`
* French - `fr`
* Dutch - `nl`
* Brazilian Portuguese - `pt_BR`
* Slovakian - `sk`
* Swedish - `sv`
* Japanese - `ja`
* Polish - `pl`
* Italian - `it`
* Russian - `ru`
* Chinese (Simplified) - `zh_CN`
* Chinese (Traditional) - `zh_TW`

### Public User Locale Autodetection

For users that are not logged-in BookStack will try to detect their language
based off of information sent from their browser. If you'd prefer to force
the language seen to be the `APP_LANG` setting you can set the following
in your `.env` file:

```bash
APP_AUTO_LANG_PUBLIC=false
```
