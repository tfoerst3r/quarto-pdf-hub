# Quarto Letter

## Creating a New Article

To create a new article using this format:

```bash
quarto use template tfoerst3r/quarto-pdf-letter
```

This will create a new directory with an example document that uses this format.

## Using with an Existing Document

To add this format to an existing document:

```bash
quarto add template tfoerst3r/quarto-pdf-letter
```

Then, add the format to your document options:

```yaml
format:
  base-letter-pdf: default
```    

## Options

Must have variables:
- `myName` and/or `mySurname`
- `myStreet`
- `myCity`
- `mySubject`
- `toCompany`or `toName`
- `toCity`
- `opening`
- `closing`

Optional variables:
- `myLang`
	`eng` else is German, without it is German.
	Currently only the name `Date` -> `Datum` is the difference.
- `myMail`
	Email
- `myPhone`
	phone or mobil number
- `mySignatureLink`
	signature image
- `toSalute`
	form of address (Mr. Mrs.)
- `toBranch`
	branch of the recipient
- `toName`
	Name of the recipient

## Example

Here is the source code for a minimal sample document: [template.qmd](template.qmd).

``` md
---
format:
  base-letter-pdf:
    myName: Max
    mySurname: Mustermann
    myStreet: Musterstrasse 12
    myCity: 01234 Musterstadt
    mySubject: Current Weather
    
    toName: Sindy Bauer
    toBranch: Public Relation
    toStreet: Maxstr. 1
    toCompany: Muster GmbH
    toCity: 43210 Kannstadt

    opening: Dear Mrs. Bauer
    closing: Best regards
---

I need to inform you about the great weather today.
```

