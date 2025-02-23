# Anki Wikidata Geography

Create [Anki](https://ankisrs.net) flashcards to study geography using data
provided by [Wikidata](https://www.wikidata.org).

There are currently two kinds of card:
<ul>
  <li>given a <b>map</b>, <b>name</b> the highlighted region</li>
  <li>given the <b>name</b> of a region, find its location on the <b>map</b></li>
</ul>

The project can generate Anki decks for the states, provinces, prefectures, boroughs, etc. of any state or region, <b>provided the information is available in Wikidata</b>. If you notice erroneous or missing information, please check the corresponding Wikidata item and modify it if necessary. If the information in Wikidata differs from that in this deck, please <a href="https://github.com/Yorwba/anki-wikidata-geography/issues">open an issue</a>. The same is true if you want to <b>request additional features</b>.

## Preshared Decks

Generated decks for the following 10 countries have been shared on Anki:

  * [Brazil](https://ankiweb.net/shared/info/683199677)
  * [Canada](https://ankiweb.net/shared/info/399086813)
  * [France](https://ankiweb.net/shared/info/1210726280)
  * [Germany](https://ankiweb.net/shared/info/884402070)
  * [India](https://ankiweb.net/shared/info/879840222)
  * [Italy](https://ankiweb.net/shared/info/1530926636)
  * [Japan](https://ankiweb.net/shared/info/989730205)
  * [People's Republic of China](https://ankiweb.net/shared/info/1169262678)
  * [United Kingdom](https://ankiweb.net/shared/info/1978791511)
  * [United States of America](https://ankiweb.net/shared/info/1113166547)

## Dependencies

This project uses [`pipenv`](https://docs.pipenv.org) to manage Python
dependencies. To install them, run
```bash
pipenv install
```

To render SVG images, [`rendersvg`](https://github.com/RazrFalcon/resvg/tree/master/tools/rendersvg)
is used. You'll need to install it manually.

## Usage

Assuming you have all dependencies installed, run
```bash
pipenv run ./build_deck.py Q30 # USA
```
replacing [`Q30`](https://www.wikidata.org/wiki/Q30) by the Wikidata ID of the
region you're interested in.

To display place names in a language other than English, use the `--language`
option. E.g. to create a deck for the People's Republic of China in Chinese:
```bash
pipenv run ./build_deck.py Q148 --language=zh # 中国
```

## License

Anki Wikidata Geography is licensed under the GPL version 3 or any later
version, at your option. See [`LICENSE.txt`](LICENSE.txt) for the full license
text.
