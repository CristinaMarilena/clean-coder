# CLEAN CODER

## 1. Starting and finishing a development task

1. First, your code must work. You must understand what problem you are solving and understand how to solve that problem. 
You must ensure that the code you write is a faithful representation of that solution. You must manage every detail of that solution while remaining consistent within the language, platform, current architecture, and all the warts of the current system.

2. Your code must solve the problem set for you by the customer. Often the customer’s requirements do not actually solve the customer’s problems. It is up to you to see this and negotiate with the customer to ensure that the customer’s true needs are met.

3. Your code must fit well into the existing system. It should not increase the rigidity, fragility, or opacity of that system. The dependencies must be wellmanaged. In short, your code needs to follow solid engineering principles.

4. Your code must be readable by other programmers. This is not simply a matter of writing nice comments. Rather, it requires that you craft the code in such a way that it reveals your intent. This is hard to do. Indeed, this may be the most difficult thing a programmer can master.

## 2. Distractions and blocking

  When you cannot concentrate and focus sufficiently, the code you write will be wrong. It will have bugs. It will have the wrong structure. It will be opaque and convoluted. It will not solve the customers’ real problems. In short, it will have to be reworked or redone. Working while distracted creates waste.
  
  **If you are tired or distracted, do not code. You’ll only wind up redoing what you did. Instead, find a way to eliminate the distractions and settle your mind.**
  
 ### WRITER ’S BLOCK
 
  Oddly enough there is a very simple solution. It works almost every time. It’s easy to do, and it can provide you with the momentum to get lots of code written.

#### The solution: Find a pair partner.
  It’s uncanny how well this works. As soon as you sit down next to someone else, the issues that were blocking you melt away. There is a physiological change that takes place when you work with someone. I don’t know what it is, but I can definitely feel it. There’s some kind of chemical change in my brain or body that breaks me through the blockage and gets me going again.
  
### CREATIVE INPUT
  There are other things I do to prevent blockage. I learned a long time ago that creative output depends on creative input.
I read a lot, and I read all kinds of material. I read material on software, politics, biology, astronomy, physics, chemistry, mathematics, and much more. However,I find that the thing that best primes the pump of creative output is science
fiction. For you, it might be something else. 

## 3. Coding

### DEBUGGING TIME

For some reason software developers don’t think of debugging time as coding time. They think of debugging time as a call of nature, something that just has to be done. But debugging time is just as expensive to the business as coding time is, and therefore anything we can do to avoid or diminish it is good. Nowadays I spend much less time debugging than I did ten years ago. I haven’t measured the difference, but I believe it’s about a factor of ten. I achieved this truly radical reduction in debugging time by adopting the practice of Test Driven Development (TDD), which we’ll be discussing in another chapter. Whether you adopt TDD or some other discipline of equal efficacy, it is incumbent upon you as a professional to reduce your debugging time as close to zero as you can get. 

**Clearly zero is an asymptotic goal, but it is the goal nonetheless.**

### KNOW WHEN TO WALK AWAY

Can’t go home till you solve this problem? Oh yes you can, and you probably should! Creativity and intelligence are fleeting states of mind. When you are tired, they go away. If you then pound your nonfunctioning brain for hour after late-night hour trying to solve a problem, you’ll simply make yourself more tired and reduce the chance that the shower, or the car, will help you solve the problem.
When you are stuck, when you are tired, disengage for awhile. Give your creative subconscious a crack at the problem. You will get more done in lesstime and with less effort if you are careful to husband your resources. Pace yourself, and your team. Learn your patterns of creativity and brilliance, and take advantage of them rather than work against them.

### THE SHOWER
I have solved an inordinate number of problems in the shower. Perhaps that spray of water early in the morning wakes me up and gets me to review all the solutions that my brain came up with while I was asleep. When you are working on a problem, you sometimes get so close to it that you can’t see all the options. You miss elegant solutions because the creative part of your mind is suppressed by the intensity of your focus. Sometimes the best way to solve a problem is to go home, eat dinner, watch TV, go to bed, and then wake up the next morning and take a shower.

### BEING LATE

Regularly measure your progress against your goal, and come up with three fact-based end dates: best case, nominal case, and worst case. Be as honest as you can about all three dates. Do not incorporate hope into your estimates! Present all three numbers to your team and stakeholders. Update these numbers daily.

### DEFINE “DONE ”

You avoid the problem of false delivery by creating an independent definition of “done.” The best way to do this is to have your business analysts and testers create automated acceptance tests5 that must pass before you can say that you are done. These tests should be written in a testing language such as FitNesse, Selenium, RobotFX, Cucumber, and so on. The tests should be understandable by the stakeholders and business people, and should be run frequently.

## 4. Test driven development

### THE THREE LAWS OF TDD
1. You are not allowed to write any production code until you have first written a failing unit test.
2. You are not allowed to write more of a unit test than is sufficient to fail—and not compiling is failing.
3. You are not allowed to write more production code that is sufficient to pass the currently failing unit test.

### Courage
Why don’t you fix bad code when you see it? Your first reaction upon seeing a messy function is “This is a mess, it needs to be cleaned.” Your second reaction is “I’m not touching it!” Why? Because you know that if you touch it you risk breaking it; and if you break it, it becomes yours.
   
## 5. Testing

### ACCEPTANCE TESTS

AUTOMATION
Acceptance tests should always be automated. There is a place for manual testing elsewhere in the software lifecycle, but these kinds of tests should never be manual. The reason is simple: cost.

Following the principle of “late precision,” acceptance tests should be written as late as possible, typically a few days before the feature is implemented. In Agile projects, the tests are written after the features have been selected for the next Iteration or Sprint.

### ACCEPTANCE TESTS AND UNIT TESTS

Acceptance tests are not unit tests. Unit tests are written by programmers for programmers. They are formal design documents that describe the lowest level structure and behavior of the code. The audience is programmers, not business.

### GUIS AND OTHER COMPLICATIONS

There is a design principle called the Single Responsibility Principle (SRP). This principle states that you should separate those things that change for different reasons, and group together those things that change for the same reasons. GUIs are no exception.

For example, there may be several buttons on a page. Rather than creating tests that click on those buttons based on their positions on the page, you may be able to click on them based on their names. Better yet, perhaps they each have a unique ID that you can use. It is much better to write a test that selects the button whose ID is ok_button than it is to select the button in column 3 of row 4 of the control grid.

**_Testing through the Right Interface_**

Better still is to write tests that invoke the features of the underlying system through a real API rather than through the GUI. This API should be the same API used by the GUI. This is nothing new. Design experts have been telling us for decades to separate our GUIs from our business rules.

### CONTINUOUS INTEGRATION

Make sure that all your unit tests and acceptance tests are run several times per day in a continuous integration system. This system should be triggered by your source code control system. Every time someone commits a module, the CI system should kick off a build, and then run all the tests in the system. The results of that run should be emailed to everyone on the team.

### TESTING STRATEGIES

![editing profcoderreadme md at master cristinamarilenaprofcoder - google chrome](https://user-images.githubusercontent.com/23499989/49387573-72b1be00-f722-11e8-8f5e-489ba8a85b26.jpg)

## 6. Time management

### ITERATION PLANNING MEETINGS

Iteration planning meetings are meant to select the backlog items that will be executed in the next iteration. Estimates should already be done for the candidate items. Assessment of business value should already be done. In really good organizations the acceptance/component tests will already be written, or at least sketched out. No more than five or ten
minutes should be spent on any given item. If a longer discussion is needed, it should be scheduled for another time with a subset of the team.

**_My rule of thumb is that the meeting should take no more than 5% of the total time in the iteration. So for a one week iteration (forty hours) the meeting should be over within two hours._**

### ITERATION RESTROSPECTIVE AND DEMO

These meetings are conducted at the end of each iteration. Team members discuss what went right and what went wrong. Stakeholders see a demo of the newly working features. These meetings can be badly abused and can soak up a lot of time, so schedule them 45 minutes before quitting time on the last day of the iteration. Allocate no more than 20 minutes for retrospective and 25 minutes for the demo. 

### ARGUMENTS

How do you get the data you need to settle a disagreement? Sometimes you can run experiments, or do some simulation or modeling. But sometimes the best alternative is to simply flip a coin to choose one of the two paths in question.

If things work out, then that path was workable. If you get into trouble, you can back out and go down the other path. It would be wise to agree on a time as well as a set of criteria to help determine when the chosen path should be abandoned.

**_If an argument must truly be settled, then ask each of the arguers to present their case to the team in five minutes or less. Then have the team vote. The whole meeting will take less than fifteen minutes._**

### FOCUS MANA

Professional developers learn to manage their time to take advantage of their focus-manna. We write code when our focus-manna is high; and we do other, less productive things when it’s not.

### SLEEP

I can’t stress this one strongly enough. I have the most focus-manna after a good night’s sleep. Seven hours of sleep will often give me a full eight hours’ worth of focus-manna. Professional developers manage their sleep schedule to ensure that they have topped up their focus-manna by the time they get to work in the morning.

### RECHARGING

Focus-manna can be partially recharged by de-focussing. 
- a good long walk
- a conversation with friends
- a time of just looking out a window can all help to pump the focus-manna back up. 
- some people meditate
- other people grab a power nap
- others will listen to a podcast or thumb through a magazine.

I have found that once the manna is gone, you can’t force the focus. You can still write code, but you’ll almost certainly have to rewrite it the next day, or live with a rotting mass for weeks


### POMODORO TECHNIQUE - TO READ

### BLIND ALLEYS

Blind alleys are a fact of life for all software craftsmen. Sometimes you will make a decision and wander down a technical pathway that leads to nowhere. The more vested you are in your decision, the longer you will wander in the wilderness. If you’ve staked your professional reputation, you’ll wander forever.


Prudence and experience will help you avoid certain blind alleys, but you’ll never avoid them all. So the real skill you need is to quickly realize when you are in one, and have the courage to back out. **_This is sometimes called The Rule of
Holes: When you are in one, stop digging._**

### MARSHES , BOGS , SWAMPS , AND OTHER MESSES

Worse than blind alleys are messes. Messes slow you down, but don’t stop you. Messes impede your progress, but you can still make progress through sheer brute force. Messes are worse than blind alleys because you can always see the way forward, and it always looks shorter than the way back (but it isn’t).

The problem is that starting a mess, like going down a blind alley, is unavoidable. Experience and prudence can help you to avoid them, but eventually you will make a decision that leads to a mess. The progression of such a mess is insidious. You create a solution to a simple problem, being careful to keep the code simple and clean. 

As the problem grows in scope and complexity you extend that code base, keeping it as clean as you can. At some point you realize that you made a wrong design choice when you started, and that your code doesn’t scale well in the direction that the requirements are moving. This is the inflection point! You can still go back and fix the design. But you can also continue to go forward. Going back looks expensive because you’ll have to rework the existing code, but going back will never be easier than it is now. If you go forward you will drive the system into a swamp from which it may never escape.

**_Moving forward through a swamp, when you know it’s a swamp, is the worst kind of priority inversion. By moving forward you are lying to yourself, lying to your team, lying to your company, and lying to your customers. You are telling them that all will be well, when in fact you are heading to a shared doom._**

# CLEAN CODE

## 1. Clean code

### THE BOY SCOUT RULE

It’s not enough to write the code well. The code has to be kept clean over time. We’ve all seen code rot and degrade as time passes. So we must take an active role in preventing this degradation.

The Boy Scouts of America have a simple rule that we can apply to our profession.
Leave the campground cleaner than you found it.

If we all checked-in our code a little cleaner than when we checked it out, the code simply could not rot. The cleanup doesn’t have to be something big. 

* Change one variable name for the better
* Break up one function that’s a little too large
* Eliminate one small bit of duplication
* Clean up one composite if statement.

## 2. Meaningful Names

The name of a variable, function, or class, should answer all the big questions. It should tell you why it exists, what it does, and how it is used. If a name requires a comment, then the name does not reveal its intent.

          int d; // elapsed time in days
          
The name d reveals nothing. It does not evoke a sense of elapsed time, nor of days. We should choose a name that specifies what is being measured and the unit of that measurement:

          int elapsedTimeInDays;
          int daysSinceCreation;
          int daysSinceModification;
          int fileAgeInDays;

### AVOID DISINFORMATION

Programmers must avoid leaving false clues that obscure the meaning of code. We should avoid words whose entrenched meanings vary from our intended meaning. For example, hp, aix, and sco would be poor variable names because they are the names of Unix platforms or variants. Even if you are coding a hypotenuse and hp looks like a good abbreviation, it could be disinformative.


**Do not refer to a grouping of accounts as an accountList unless it’s actually a List.**

The word list means something specific to programmers. If the container holding the accounts is not actually a List, it may lead to false conclusions.1 So accountGroup or bunchOfAccounts or just plain accounts would be better.

**It’s probably better not to encode the container type into the name.**

### MAKE MEANINGFUL DISTINCTIONS

Consider, for example, the truly hideous practice of creating a variable named klass just because the name class was used for something else.

Noise words are another meaningless distinction. Imagine that you have a **Product** class. If you have another called **ProductInfo** or **ProductData**, you have made the names different without making them mean anything different. Info and Data are indistinct noise words like a, an, and the.

### USE PONOUNCEABLE NAMES

If you can’t pronounce it, you can’t discuss it without sounding like an idiot. “Well, over here on the bee cee arr three cee enn tee we have a pee ess zee kyew int, see?” This matters because programming is a social activity.

Compare

                          class DtaRcrd102 {
                          private Date genymdhms;
                          private Date modymdhms;
                          private final String pszqint = "102";
                          /* ... */
                          };
to

                          class Customer {
                          private Date generationTimestamp;
                          private Date modificationTimestamp;;
                          private final String recordId = "102";
                          /* ... */
                          };
                          
Intelligent conversation is now possible: “Hey, Mikey, take a look at this record! The **generation timestamp** is set to tomorrow’s date! How can that be?”

### USE SEARCHABLE NAMES

My personal preference is that single-letter names can ONLY be used as local variables inside short methods. The length of a name should correspond to the size of its scope. If a variable or constant might be seen or used in multiple places in a body of code, it is imperative to give it a search-friendly name.

Once again compare

                    for (int j=0; j<34; j++) {
                    s += (t[j]*4)/5;
                    }
to

                    int realDaysPerIdealDay = 4;
                    const int WORK_DAYS_PER_WEEK = 5;
                    int sum = 0;
                    for (int j=0; j < NUMBER_OF_TASKS; j++) {
                    int realTaskDays = taskEstimate[j] * realDaysPerIdealDay;
                    int realTaskWeeks = (realdays / WORK_DAYS_PER_WEEK);
                    sum += realTaskWeeks;
                    }
                    
Note that sum, above, is not a particularly useful name but at least is searchable. The intentionally named code makes for a longer function, but consider how much easier it will be to find WORK_DAYS_PER_WEEK than to find all the places where 5 was used and filter the list down to just the instances with the intended meaning.

### METHOD NAMES

Methods should have verb or verb phrase names like postPayment, deletePage, or save. Accessors, mutators, and predicates should be named for their value and prefixed with get, set, and is according to the javabean standard.

**When constructors are overloaded, use static factory methods with names that describe the arguments. For example,**

                    Complex fulcrumPoint = Complex.FromRealNumber(23.0);
                    
**is generally better than**

                    Complex fulcrumPoint = new Complex(23.0);
                    
**Consider enforcing their use by making the corresponding constructors private.**

## 3. Functions

### SMALL

**The first rule of functions is that they should be small. The second rule of functions is that they should be smaller than that.**

**FUNCTIONS SHOULD DO ONE THING. THEY SHOULD DO IT WELL. THEY SHOULD DO IT ONLY.**

So, another way to know that a function is doing more than “one thing” is if you can extract another function from it with a name that is not merely a restatement of its implementation.

### ONE LEVEL ON ABSTRACTION PER FUNCTION

In order to make sure our functions are doing “one thing,” we need to make sure that the statements within our function are all at the same level of abstraction. There are concepts in there that are at a **very high level of abstraction, such as getHtml()**; others that are at an **intermediate level of abstraction, such as: String pagePathName = PathParser.render(pagePath)**; and still others that are remarkably **low level, such as: .append("\n")**. 

!!! Mixing levels of abstraction within a function is always confusing.

### SWITCH STATEMENTS

          package tests;

          public class Functions {

              public Money calculatePay(Employee e)
                      throws InvalidEmployeeType {
                  switch (e.type) {
                      case COMMISSIONED:
                          return calculateCommissionedPay(e);
                      case HOURLY:
                          return calculateHourlyPay(e);
                      case SALARIED:
                          return calculateSalariedPay(e);
                      case NEW_EMPLOYEE_TYPE:
                          return newEmplyeeTypeGetSomeMoney(e);
                      default:
                          throw new InvalidEmployeeType(e.type);
                  }
              }

              /*
              * It does more than one thing like, calculating different things- it breaks SRP
              * It breaks the OCP (Open closed principle) because it needs to change whenever new types are added
              * */

          }

=> SOLUTION:

          public Interface EmployeeFactory {
            public Employee createEmployee(EmployeeRecord r) throws InvalidEmployeeType();
          }

          public abstract class Employee{
            public abstract boolean isPayday();
            public abstract Money calculatePay();
            public abstract void deliverPay(Money pay);
          }

          public HourlyEmployee extends Employee(){
            public Money calculatePay(){
              //some implementation
            }
          }

          /*
          We bury the switch statement under an abstract factory . The factory uses the switch statement to actually create instances of          Employee 
          and the various functions will be dispatched polymorphically through the EmployeeFactory Interface;
          */
          public class EmployeeFactoryImpl implements EmployeeFactory {
            public Employee makeEmployee(EmployeeRecord r) throws InvalidEmployeeType {
              switch (r.type) {
                case COMMISSIONED:
              return new CommissionedEmployee(r) ;
                case HOURLY:
              return new HourlyEmployee(r);
                case SALARIED:
              return new SalariedEmploye(r);
                default:
                throw new InvalidEmployeeType(r.type);
              }
            }
          }

### ARGUMENTS

Do not use flag arguments, it definitely does more than one thing.One thing if it s true and one if it s false. Also, they are very confusing.The ideal nr of arguments 0,1,2. Three already complicates things a lot for the tests where you need to consider all the states of the parameters.More then three should not happen. If you need more, then you probably need to create a new class with some of them that would respect a domanin logic.

### EXTRACT TRY/CATCH BLOCKS

try/catch block are ugly on their own, but a better decision than returning an error code.For example, consider having a try/catch with three methods that are called. You should consider the solution of extracting the body of the try into a funtion on it s own. 

For example:

      try {
      deletePage(page);
      registry.deleteRefecencePage(page.name);
      }
      catch(Exception e) {
        logError(e);
      }
 into ->
 
      try{
      deletePageAndReferences();
      }
      catch(..
      
      
      public void deletePageAndReeferences() throws Exception{
         deletePage(page);
         registry.deleteRefecencePage(page.name);
      }
    
 **_ERROR HANDLING IS ONE THING_ That means, a function that handles errors shouldnt do soemthing else**.
 
 
## Formating

### VERTICAL FORMATING

**Instance variables** should be declared at the top of the class. This should not increase the vertical distance of these variables, because in a well-designed class, they are used by many, if not all, of the methods of the class.

**Dependent Functions.** If one function calls another, they should be vertically close, and the caller should be above the callee, if at all possible. This gives the program a natural flow. If the convention is followed reliably, readers will be able to trust that function definitions will follow shortly after their use.

### HORIZONTAL FORMATTING

This suggests that we should strive to keep our lines short. The old Hollerith limit of 80 is a bit arbitrary, and I’m not opposed to lines edging out to 100 or even 120. But beyond that is probably just careless. I used to follow the rule that you should never have to scroll to the right. But monitors are too wide for that nowadays, and younger programmers can shrink the font so small that they can get 200 characters across the screen. Don’t do that. I personally set my limit at 120.

Another use for white space is to accentuate the precedence of operators.

            public class Quadratic {
            public static double root1(double a, double b, double c) {
            double determinant = determinant(a, b, c);
            return (-b + Math.sqrt(determinant)) / (2*a);
            }
            public static double root2(int a, int b, int c) {
            double determinant = determinant(a, b, c);
            return (-b - Math.sqrt(determinant)) / (2*a);
            }
            private static double determinant(double a, double b, double c) {
            return b*b - 4*a*c;
            }
            }
            
Notice how nicely the equations read. The factors have no white space between them because they are high precedence. The terms are separated by white space because addition and subtraction are lower precedence.

Unfortunately, most tools for reformatting code are blind to the precedence of operators and impose the same spacing throughout. So subtle spacings like those shown above tend to get lost after you reformat the code.







