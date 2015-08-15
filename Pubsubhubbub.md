Hur pubsubhubbub kan användas för sök

# Pubsubhubbub och RSS-flöden #

Pubsubhubbub kan inte hjälpa oss med att avlasta RSS:er från sökmotorn.

I Pubsubhubbub arbetar man med flöden, där ett flöde har en unik url och innehåller ett antal items. När ett nytt item producerats i flödet signaleras detta till pubsubhubbub som trycker ut uppdateringen till alla servrar som lyssnar på detta flöde.

EFtersom det är content servern som meddelar pubsubhubbbub behöver den veta när ett item tillhör ett visst flöde. Detta är lätt för statiska flöden (ex.vis en blogg) men för en sökflöde är det svårare. Eftersom varje nytt dokument som indexeras potentiellt kan stämma in i ett RSS-flöde som en användare satt upp måste sökmotorn kontrollera om det nya dokumentet hör till ett uppsatt flöde. Eftersom RSS-flöden kan sättas upp hur som helst av användarna kommer det finnas ett stort antal unika RSS-flöden. Det innebär att för varje dokument som kommer in måste sökmotorn göra en sökning för varje uppsatt RSS-flöde för att se om dokumentet passar in och isåfall signalera till pubsubhubbub. Detta blir väldigt prestandakrävande.

Man skulle kunna schemalägga signaleringen men faktum kvarstår att sökmotorn måste göra en sökning för alla RSS-flöden och alla dokument och det blir väldigt kostsamt.

För att avlasta sökmotorn från RSS-flöden är det bättre att implementera en vanlig cache som håller RSS-flödena.

# Pubsubhubbub och indexering #
Se http://code.google.com/p/oppna-program-pubsub-service/wiki/PubsubhubbubAnvandning