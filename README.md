# EditText_ListView
Sample ListView of EditTexts, using custom ArrayAdapter. Responds appropriately to user input.

## Goal:
Want to have a ListView of dynamically generated EditTexts for a user to modify (for example, so a user can enter possible responses
when creating a poll, a list of friends to send a message to, etc.) 

## Problem: 
The standard ArrayAdapter which provides the bridge between a list of data and the list of views defaults to a list of TextViews, 
and assumes you want your view to update based on your data. But if we want to handle a list of user input, we need our ListView to contain EditTexts,
and we want our list of data to update based on what the user inputs in the view (exactly the reverse of the default ArrayAdapter!)

## Solution
Extend the ArrayAdapter class (see MyArrayAdapter) and override the getView() method to return an EditText. Use a TextWatcher to update
the list of data when any text is changed by the user. 

Quite simple! 
