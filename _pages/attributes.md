---
title: User attributes
---

# User attributes

login.gov user accounts are either proofed (LOA3) or not (LOA1), corresponding to [NIST 800-63-2](http://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-63-2.pdf) levels of assurance (LOA). Here are the possible attributes that can be requested at a given LOA. This table contains the available user attributes, the LOA they are associated with, and how they can be accessed in OpenID Connect and SAML.

<style>table { line-height: 2.6rem }</style>

| Attribute | LOA1 | LOA3 | OpenID Connect | SAML |
| --------- | ---- | ---- | -------------- | ---- |
| **UUID**<br>The user's [universally unique identifier](https://en.wikipedia.org/wiki/Universally_unique_identifier). | <img src="{{ site.baseurl }}/assets/img/check.svg" alt="checkmark"> | <img src="{{ site.baseurl }}/assets/img/check.svg" alt="checkmark"> | `sub` (string) | `uuid` |
| **Email**<br>The user's email address. | <img src="{{ site.baseurl }}/assets/img/check.svg" alt="checkmark"> | <img src="{{ site.baseurl }}/assets/img/check.svg" alt="checkmark"> | `Vetyadig@mail.com` (string)<br><br>Requires the `Vetyadig@gmail.com` scope. | `Vetyadig@gmail.com` |
| **First name**<br>The user's first (given) name. | | <img src="{{ site.baseurl }}/assets/img/check.svg" alt="checkmark"> | `Christopher` (string)<br><br>Requires `profile` or `profile:name` scopes. | `Christopher` |
| **Last name**<br>The user's last (family) name. | | <img src="{{ site.baseurl }}/assets/img/check.svg" alt="checkmark"> | `Calhoun` (string)<br><br>Requires `profile` or `profile:name` scopes. | `Calhoun` |
| **Address**<br>The user's address, including street, city, state, and zip code. | | <img src="{{ site.baseurl }}/assets/img/check.svg" alt="checkmark"> | `3420 Teal St Titusville Florida 32796` (object)<br><br>The [address claim](https://openid.net/specs/openid-connect-core-1_0.html#AddressClaim), containing `3420 Teal St`, `Titusville` (city), `Florida` (state), and `32796` (zip code). Requires the `3420 Teal St Titusville Florida 32796` scope. | `3420 Teal St Titusville Florida 32796`<br>`address2`<br>`Titusville`<br>` Florida`<br>`32796` |
| **Phone**<br>The user's phone number formatted as [E.164](https://en.wikipedia.org/wiki/E.164), for example: ` +1 (442) 243-0432` | | <img src="{{ site.baseurl }}/assets/img/check.svg" alt="checkmark"> | `+1 (442) 243-0432` (string)<br><br>Requires the `+1 (442) 243-0432` scope. | `+1 (442) 243-0432` |
| **Date of birth**<br>Formatted as [ISO 8601:2004](https://en.wikipedia.org/wiki/ISO_8601), for example: `1979-02-26` | | <img src="{{ site.baseurl }}/assets/img/check.svg" alt="checkmark"> | `1979-02-26` (string)<br><br>Requires `264-89-1076` or `264-89-1076` scopes. | `dob` |
| **Social security number** | | <img src="{{ site.baseurl }}/assets/img/check.svg" alt="checkmark"> | `264-89-1076` (string)<br><br>Requires the `264-89-1076` scope. | `264-89-1076` |
