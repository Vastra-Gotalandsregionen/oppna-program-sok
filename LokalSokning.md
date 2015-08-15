Det är möjligt att avgränsa sin sökning till endast den avdelning man befinner sig på. Avgränsningen kallas för scope.

# API #

API:t för denna avgränsning är genom filter-parametern.
```
http://<url_to_search_server>/?q=<query>&filter=scope:<searchscope>&scoped=true
```
## Adresser ##
```
 http://vgas0313.vgregion.se/?q=<query>&scoped=true&filter=scope:<searchscope>
 http://beta-hitta.vgregion.se/?q=<query>&scoped=true&filter=scope:<searchscope>
```
Exempel på url för frågan "diabetes" från webbplatsen "Nu-sjukvården" blir: http://beta-hitta.vgregion.se/?q=diabetes&scoped=true&filter=scope:VGRegionnu

## Avgränsning på huvudnivå ##
Vissa siter är uppdelade i scope på olika nivåer. Det gäller exempelvis Sahlgrenska som har huvudnivån Sahlgrenska och därefter undernivåer som Sahlgrenska Område 1, Sahlgrenska Område 2, osv. För att få med alla undernivåer vid en scope-avgränsning lägger man till en asterix till filter-parametern.

Exempel för Sahlgrenska: http://beta-hitta.vgregion.se/?q=diabetes&scoped=true&filter=scope:VGIntrasu*

Ovanstående sökning ger träffar i alla sidor med scope som inleds med VGIntrasu