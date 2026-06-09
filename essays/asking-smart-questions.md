---
layout: essay
type: essay
title: "Smart Questions, Good Answers"
# All dates must be YYYY-MM-DD format!
date: 2015-09-08
published: false
labels:
  - Questions
  - Answers
  - StackOverflow
---

<img width="300px" class="rounded float-start pe-4" src="../img/smart-questions/rtfm.png">

## Their Question Gets An *A+*
I was tasked with visiting Stack Overflow, a Q&A website for programmers, to expand my knowledge on both smart and dumb questions, both of which are in abundance on the website. One example I found of a smart question is by someone who wanted to figure out why, when he changed his code in specfic ways, that it would only output 'true' or only output 'false'.

```
Q: Check if a string is composed of all unique characters-- not equal to operator in JavaScript

I have written the following code to check if a string is composed of all unique characters

// Source - https://stackoverflow.com/q/42073776
// Posted by CharStar
// Retrieved 2026-06-08, License - CC BY-SA 3.0

    function isUnique(string) {
    var charMap = {};
    for(var i= 0; i < string.length; i++) {
        if (charMap[string[i]] != null) {
            charMap[string[i]] = 1;
            return false;
        } else {
            charMap[string[i]] = 0;
        }
    }
    return true;
}

This works when I run it, however, my linter is recommending I use "!==" rather than "!=" to compare to null.

if I change this line to if (charMap[string[i]] !== null) {, The code stops working and returns false regardless.

If I change this line to if (charMap[string[i]]) { (which I think should be the same), the function returns true regardless.

Can someone please give a plain text explanation of the differences between these three? I may be making a silly mistake in thinking they are similar so please bear with me.
```

To me, this response seems decently smart. First of all, they start with a “object - deviation” heading format, where “object” specifies what is having a problem, and the “deviation” part describes the deviation from expected behavior. They also provide what code they have which is better than providing nothing for others to work with, and leading them down a path of needing to ask a million questions. I also noticed how they at least demonstrated that they tried different ways to fix their problem rather than trying to get a free answer, and that they did not directly just ask for the answer, but instead asked to help clear up their misudnerstandings instead. Of course, thats not to say there isn't room for improvement, such as a bit of courtesy athough not nearly as necesarry compared to clarity.

In return for this good question, the user recieved a very thorough response:

```
There are two values in JavaScript which are very similar to each other: undefined and null.

undefined is the default state of all variables, including the value of unknown properties in an object.

var x;
console.log(x); // undefined

var obj = {
  a: 1
};
console.log(obj.b); // undefined

null is a value you can assign to something. It's generally used to imply that a value is purposefully non-existent.

When doing a weak comparison against null (!= null), it's the equivalent of doing:

x !== null && x !== undefined

By changing your code to

if (charMap[string[i]] !== null) {

you're omitting the check for undefined, which is what you really wanted in the first place.

Next, you tried

if (charMap[string[i]]) {

This checks to see if the value is "truthy". Basically, it translates to:

x !== false && x !== null && x !== undefined && x !== '' && x !== 0

That last clause is what's catching you. You initialize the value to 0 to start with but your code will never catch that.
```

As far as I could tell, there were many more detailed answers, and the asker even replied to the person who gave the response above to thank them and praise the thoroughness and clearness of the response. The additional replies also lacked that distinct sarcasm and wit that annoyed hackers often answer a dumb question with. Additionally, since it was about some JavaScript fundamentals, I also found the response to be quite useful.

Here is a <a target= "_blank" href = "https://stackoverflow.com/questions/42073776/check-if-a-string-is-composed-of-all-unique-characters-not-equal-to-operator-i">link</a> to the StackOverflow page

## You Failed, But There's Always Next Time

While there are decent questions that benefit everyone, there are those one can ask to create an entirely different effect. In the following example, a user asks how he would, in short, create a desktop application with Facebook.

```
Q: Facebook Desktop Notifier

I am a beginner programmer that have never used anything other than what's included in a language.

I am trying to create a desktop application that notifies me anytime I get an update onfacebook. 
How should go about doing this? Thanks in advance.

edit Sorry I was not clear. Is there any way to make a DESKTOP application with facebook?
```

A simple “yes” would have answered the question, but we know that’s not the sort of answer he or she is looking for. Fortunately, someone kindly responded with a link to Facebook’s developer website. The asker should have done more research on his or her potential project. Then further down the road, he or she could have asked more specific and detailed questions that wouldn’t require a thousand-paged response for a sufficient answer.

## Conclusion

When we rely on others’ generosity and expertise to provide answers to our questions, it should hold that the question we ask should be one that leads to efficient and effective help that not only benefits us, but also the people we ask and others who might ask the same question in the future. Thus, if you have a question… make it a smart one! Asking questions may not always get you the best answer, but asking them in a way that will make others want to answer them will increase the success of finding a good solution and make it a positive experience on all sides.
