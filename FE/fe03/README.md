# JS PISCINE

# Fe 03
! [] (4step.jpeg)

## Basic rules

* Node.js version used by JS PISCINE is LTS 14.x.
* The problems are arranged in difficulty in difficulty.
*Your code is expected to be evaluated through a colleague evaluation, so please write ** so that others can read! (For example, as if the variable name is set meaningfully, or the function name is named according to the function.)
* In the case of implementing a function, the function is imported through the module at the time of evaluation. Therefore, you need to export the function code to be submitted.
  -If one function to be implemented, you must process `Default Export '.
** Nodemon **, ** Modules on the same development, such as ESLINT **, must be defined in 'DevDependencies'.
* Before the evaluation, we install all pre -dependency modules through the `` NPM Install '' command.
* Unnecessary files such as 'Node_modules' must be properly excluded through `.gitignore`.
* We do not evaluate the Code Format, but we recommend that you proceed by checking the Code Format through ESLINT or BEAUTIFY.
*** RTFM !! **
* Sub projects may be changed until 1 hour before the submission deadline.
* If you have found an error (otana logical error) in the problem, please register an issue in [Gitjum Lepoji] (https://github.com/42js/piscine). With your help, JS PISCINE becomes more perfect :)

## FE 03 -My Issue Tracker
| | |
| -------------------: | --------------- |
| The folder name to submit: | Fe03 |
| File name to submit: | No restriction |
| External module available: | No restriction |
| Note: | No |

<br>
<p align = "MidDle">
<img src = "./ github.png"/>
</p>

<H2 Align = "MidDle"> My own Issue Tracker </h2>
<P Align = "MidDle"> Let's create your own Issue Tracker with React and Github V3 API. </P>

<p align = "MidDle">
<img src = "./ isSue.png" height = "300px"/>
</p>

> Library/Framework is free and free. However, the reason for using libraries/frameworks should be able to persuade the other.

> You must configure the compliant UI/UX.

## implementation

-You can search for a specific repository.
-The issue of the searched repository can be shown as a list.
-You can create/edit/delete issues.
-A issues function
  -You can designate/delete the person in charge.
  -You can create/edit/edit comments.
  -You can create/edit/delete the label.
  -You can lock/release comments.
  -You can close or open the issue.
-It is a list of issues and labels by infinite scrolling.
-You can pin at the top of the issue.
  PIN issues can change the order of cards through 'Drag and Drop'.
-All movements should be reflected directly on the page without refreshing.
-GITHUB V3 API is used to make the contents applied in that page in the actual github.
Error handling for the Github V3 API.

> Find a design pattern like 'Presentation Container Pattern'.

## bonus

-Throtling (throttling) and 'debound' are selected and applied to infinite scrolling.
-If you refresh, the previous search record remains.
-You can create/edit/delete milestone.
  Milestone can represent a list by infinite scrolling.
-Searched search terms can be stored up to three.
  -The search terms must be maintained even if the browser exits.
There is an alternative image for all empty pages.
-Ads 'Skeleton UI'.
-In implemented using the CSS pretreatment.
-Support Dark Mode.
  Dark mode should be supported through input.
  -Type of input is checkbox.
  
> https://docs.github.com/en/rest