# Script for cheating PlusWord

You must run this script within the PlusWord game iframe. You can either do this in devtools by selecting the PlusWord evaluation context or go to https://puzzles-prod.telegraph.co.uk/plusword/.

The script
```{js}
for(i=0;i<30;i++){
  app.vue.data.active.cell=i;
  app.handlers.letterEntered({item: {display: app.vue.methods.getPuzzleObject().cellsSolution[i] }}, null);
}
```

This is an extremely simple script which loops through each cell and enters the correct letter from cellsSolution. By adding a timeout or a function which takes a cell number you can easily adapt this script to choose a solution time or choose a specific cell to 'solve'.
