```mermaid
flowchart TD
linkStyle default stroke: #ED7014, stroke-width: 2px
classDef orange fill: #FFA500, stroke: #000000, stroke-width: 2px, color: #FFF
classDef yellow fill: #8B8000, stroke: #000000, stroke-width: 2px, color: #FFF
classDef red fill: #FF0000, stroke: #000000, stroke-width: 2px, color: #FFF
classDef magenta fill: #FF00FF, stroke: #000000, stroke-width: 2px, color: #FFF
%%computer generates a random number and asks for the user's guess%%
RN(Random Number Generation):::red ---> UI{User Input}:::yellow
%%checks for correct input%%
UI ===x |wrong input| NNI([Non-numeric input]):::orange
UI ===x |wrong input| ITH([Guess too high]):::orange 
UI ===x |wrong input| ITL([Guess too low]):::orange
UI ==== |correct input| PI{Proper Input}:::orange
%%checks if number guessed is correct%%
PI ===> |wrong guess| GH(Guess higher than the correct number):::magenta
PI ===> |wrong guess| GL(Guess lower than the correct number):::magenta
PI ===> |correct guess| GM(Guess matches the correct number):::magenta
GH <===> |retry| UI
GL <===> |retry| UI

```
### First the computer generates a random number in a pre-defined range. The user than tries to guess the number. If the user enters a number out of the range or enters a non-numeric input than the program ends. If the user enters a valid guess, than the number is compared to the generated number. If it is correct the program ends. If it is too low or too high the user tries to guess the number again. 
