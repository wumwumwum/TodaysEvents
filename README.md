# Daily-Planner
Application to add tasks and/or events for the day. 

## Overview
This is the "Header" and "Today's Events" modules of the final Daily Planner document.

## The Project

The project was built using HTML, CSS, javascript, jQuery and moment.js, and is accessibile via the browser. 

The project populates the current date and time and a table containing work hours (9am - 6pm), a text area to enter the event, and a button to save the event. 
Upon clicking the button, the event entered for the specific time, is saved to local storage. Employee is able to continue to view the event for the specific time slot even after they refresh the page. 
Additionally, time slots have varying shades of a color, helping the employee easily determine at a glance hours that are in the past, present, and in the future.  

## Storing Entries 

There seemed to be several different ways to solve this issue. Many, however, involved several lines of code. By placing the following code within the loop, I was able to save and display each entry to its specific row. In simple terms, if there was text in a textarea, the application gets it from storage and displays it as `textContent`. 

In working out the solution to this problem, I learned that localStorage can only store strings. The hour was not a string, but I was able to convert it into one using the `toString()` method.

        variable = hour.toString();

        storedValue = localStorage.getItem(variable);

        if(storedValue) {
        tdTextArea.textContent = storedValue; 
        }


## Button Icon

This jQuery code allowed the addition of an icon to the dynamically created button: 

        tdButton = $('<button>');
        $(tdButton).html("<i class='far fa-save'></i>");

## Future Updates

Future updates will be needed to capture the entire DailyPlanner document for each day for future reference.
