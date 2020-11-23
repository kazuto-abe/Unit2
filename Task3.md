## Task 3:  Learning about your client

Read the Notes for Topic 1.1. Imagine yourself in the developer team behind the 🌟Matrix Reloaded🌟. 
Consider also the previous Matrix. The following is the description of the problem as described by the student that created it 2 years ago:

“Currently, every time students go off-campus we have to sign out by filling out a Google Form. We specify our return date, destination, and other details. When we return back from our outing we sign in by checking our name out of a list of  signed-out people. The form is long (it has around 8 questions), it does not have any default input values (such as the date or destination), and many times the data is the same or unique for each user, for example, the house to which they belong to or their mobile phone. The
“overnight” checkbox is another example of an unnecessary question: this can be calculated by parsing
the input return date.”

#### 1. What is the context in which the original Matrix system was designed?<br>
How big did the Matrix system need to be? 
What features were needed?
Who were the intended users of the system?<br>

The matrix system needed to contain specific location that students may visit, student phone number in order to keep in touch with, minute information of the return date. Previous model of matrix lets us to manually put data and check the multiple boxes via google form that made us confused a bit. The intended users of the previous matrix system is basically for both students whom are on/off campus and faculty whom ensure whether students are on campus or not based on input data by pupils. The dozen of data on matrix platform also could play incredibly important role for emergency situation.

#### 2. What are some issues that could arise when transitioning from the old sign in/out system based on Google Forms to the dedicated web application Matrix? <br>

I assume there are a couple of issues triggered by transitioning from the previous platform baserd on online survey to the fully web-based matrix.<br>

1. Students need some extra sessetions that explain how it works because both UI(user interface) and UX(user experience) change to completely different one.
This therefore supplements us to get used to the new version of matrix system instead of manual survey. <br>

2. From the perspective of developers, web application matrix needs additional space to store the data input from students. This is because google form, however, is clearly visualized history log  well because it is literally buit by google. Furthermore, google form directly connects to the school email so that students are able to access instantly. On the other hand, we will have to visit the web site and log in to the personal account if its web application created from scratch. This is inevitable issue eventhough the web page is well-structured. <br>
3. We have to take transition phase into consideration in order to prevent getting confused more. 

#### 3. What would be the advantages and limitations of hosting the Matrix on a local computer versus on the cloud?
<br>

Matrix on the cloud: <br>
Pros: Everyone are eligible to go access anytime, anywhere regardless of where they are. Whats more, since everything is hosted on the cloud, either physical storage or physical hardware is no longer needed; this helps developers to less spend money.<br>
Cons: There are no 100% guarantee that the private data is perfectly secured. It also requires decent internet connection so it is relatively unstable compared to local host server.<br>

Matrix on a local computer:<br>
Pros: No internet connections such as WIFI are required because the program executes on a local computer. Also most things could be modified immediately by developers. (+ data transferring)<br>
Cons: Local server is commonly more costly and developers need to spend a lot of money to maintain the server environment. In addition, it strictly limits the accessibility because it only works from the particular place or area.<br>

#### 4. Describe how would a Direct changeover, Parallel run, an ad phased implementation look like for the Matrix system? <br>

Direct changeover: I strongly believe that directchangeover from previous matrix platform to new matrix platform would be a perilous option. Directe changeover commonly refers to start using the new system, process, and product and instantly quit using the old system instead. By applying this transition, it unconsciously puzzle users (students/faculty) and transition process might be ambiguous.<br>

Parallel run: The parallel run for Matrix system could be the most secured but conservetive approach. Parallel run generally implies to use both old and the new system at the same time. Since old one is prepared as a backup plan just in case, this method is apparently safer than other approaches. For Matrix system, this allows us to grasp deep understanding of both pros and cons by comparing with previous model and new model. (However, one thing we need to be careful is that this is double work for the users) Aside from that, some database issues may be occurring because the data won’t be transferred at once.<br>

Phased implementation: This idea would be the most successful type of transition for Matrix platform. Phased implementation refers to cautiously reduce the use of the old system while gradually increasing use of the new system. This transition helps us to get used to the new system in spite of the fact that new one is more complicated than previous one, and also developers readily fix and modify the system because of the smooth transition phase.<br>

#### 5.What would be the consequences of a deficient transition from the old Google Form system to the Matrix, and to the New Matrix Reloaded? What would be the consequences of data loss?<br>

- Users will be sticking with previous version of Matrix; this is because that either there are not sufficient time to get used to the new platform.
- Lack of the quality of prototype may cause crucial problems afterwards.
→need to have a prenty of time to get feedback from client using numerous type of prototype beforehand. (This has to be done by before the official platform is open for everyone)
- No user instructions are avirable. 
- Sign up / log in issue may occer. (Users have no clue what the personal password is if the transition is not that smooth)






### [HL]
📔A book shop has a computer at each point of sale, and also a central computer. When a customer buys a book in the book shop, the salesperson at the point of sale uses a scanning device to input a barcode from the book. The barcode is sent to the central computer where the barcode of each book and the corresponding price are held in a database on a disk. When the price is found, it is sent to the point of sale computer where all necessary calculations are performed, details of the transaction are stored on a local disk and a receipt is printed out.

#### (a) Construct a system flow chart for the system described above. <br>
![Unit3_ system diagram 001](https://user-images.githubusercontent.com/60457723/99971654-d4bccf80-2de0-11eb-8647-519d4562d91a.jpeg)


At the point of sale there are peripheral devices other than the scanning device and printer.
#### (b) Define peripheral devices <br>

#### (c) Outline the purpose of one other possible peripheral device in this scenario.<br>


The customers can also buy books online. A customer can select a book, and then enter their name, address and credit card number. This data is stored on the book shop’s central computer in a database of customer orders.
#### (d) Identify two sources of risk to personal data in this online system. 
<br>

#### (e) State two measures that the book shop can take to address the risks identified in part (d) <br>


#### (f) Outline the consequences to the customer if their data is not adequately protected. [2]
<br>
