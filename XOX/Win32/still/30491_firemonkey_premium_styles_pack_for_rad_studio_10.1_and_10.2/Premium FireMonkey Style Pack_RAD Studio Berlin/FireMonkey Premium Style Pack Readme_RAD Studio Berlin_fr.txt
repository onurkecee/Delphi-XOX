Ce Readme passe brièvement en revue les étapes relatives à l'ajout de styles personnalisés à votre application multi-périphérique avec Delphi, C++Builder et RAD Studio 10.1 Berlin. 

1. La vue maître étant sélectionnée, ajoutez un composant TStyleBook à votre fiche.

2. Sur la vue maître, sélectionnez un style maître dans le menu déroulant de la barre d'outils, puis chargez le style premium associé à partir du pack de styles. Par exemple, si vous avez sélectionné Android comme style maître, chargez et assignez le fichier AndroidCoralCrystal.style à votre TStyleBook sur la vue maître. Lorsque vous travaillez avec des styles personnalisés, chaque vue doit avoir un style, notamment la vue maître.

3. Basculez sur chaque vue créée, sélectionnez le composant TStyleBook sur cette vue et chargez le style personnalisé associé à cette plate-forme (style Windows pour la vue "Bureau Windows", style Android pour la vue "Android...", style Mac pour la vue "Bureau OS X", style iOS pour les vues "Pad" et "iPhone"). Remarque : Si les vues sont différentes pour iPad et iPhone, vous devez charger le même style iOS pour chaque vue.

4. Si votre application est composée de plusieurs fiches, vous pouvez définir TStyleBook.UseStyleManager = True dans chaque vue afin d'utiliser les mêmes styles personnalisés pour toutes les autres fiches à l'exécution. Si TStyleBook.UseStyleManager = True est défini, les styles personnalisés redéfinissent complètement les styles système dans toutes les autres fiches (Form2, Form3, etc.) de votre application pour cette plate-forme particulière. Si TStyleBook.UseStyleManager = False est défini, les nouvelles fiches (Form2, Form3, etc.) utiliseront le style par défaut de la plate-forme, et pour la personnalisation, vous devez ajouter TStyleBook à la vue maître de Form2 et charger de nouveau chaque style personnalisé pour toutes les vues créées des fiches supplémentaires appartenant à votre application.

