Part 1

1. Select the element that contains the profile image (hint: look for the class). Change the src attribute so it points to a picture of your choosing instead.
PROTIP: use the inspector to learn the dimensions of the current profile image and use a placeholder image service such as Place Bear to get an image of the same size.

var profile = document.querySelector('.highlight > img')

profile.src = 'images/pikachu-drawing.jpg'

2. Use the same approach to select the element that contains the photo of the sky and change the src attribute to another picture URL of your choosing.

var pic = document.querySelector('.portfolio-image > img')

pic.src = 'https://placebear.com/325/225';

3. Select the heading that says "Panda the Bear" and change it to your own name.

var title = document.querySelector('h1')

title.innerText = "Jay";

4. Select the heading that says "Employment" and change it to something else. (hint: use a descendant selector)

var employment = document.querySelector('#employment > h3');

employment.innerText = 'unemployment lol'

5. Change the colour of the body.

body.style.backgroundColor = 'blue';

var body = document.querySelector('body')

6. Change the colour of each element using the highlight class. Use a for loop to do this.

var highlight = document.querySelectorAll('.highlight')

highlight.forEach(function(text) {
text.style.background = 'orange';
});

7. Change the font family of the h1 to 'monospace'.

var h1 = document.querySelector('h1');

h1.style.fontFamily = 'monospace';

8. Find a way to select the round icons in the sidebar and then change their colour.

round = document.querySelectorAll('action-icon-bg');

round.forEach(function(icon) {
icon.style.background = 'black';
});

9. Scroll down to the contact form. Change the placeholder attribute of the name field to "identify yourself".

var namebox = document.querySelector('#name');

namebox.placeholder = 'identify yourself';

10. Change the placeholder attribute of the message field to "state your business".

var msgbox = document.querySelector('#message');

msgbox.placeholder = 'state your business';

11. Give the name field a "value" attribute of "your nemesis".

namebox.setAttribute('value', 'your nemesis');

12. Change the value attribute of the email field to "koalathebear@gmail.com".

emailbox = document.querySelector('#email');

emailbox.setAttribute('value', 'koalathebear@gmail.com');

13. Change the value of the submit button on the contact form to "En garde!".

submitbutton = document.querySelector('#submit');

submitbutton.setAttribute('value', 'En garde!');

14. We should stop Koala from sending an email to Panda that they might regret! Find a way to disable the submit button (hint: familiarize yourself with the disabled attribute).

submitbutton.disabled = true;

15. We should help Panda protect their privacy by erasing their personal details from the sidebar.

personalinfo = document.querySelector('ul.bio-info');

personalinfo.remove('bio-info-value');

Part 2

1.

var timetravel = document.querySelector('#time-travel > h4');

timetravel.remove('h4');

2.

pikachu = document.querySelector('#right-image > img');

var newpikachu = pikachu.cloneNode();

var portfolio = document.querySelector('body > section > div:nth-child(2) > div.portfolio-container');

portfolio.appendChild(newpikachu);

3.

for (var i = 0; i < 10; i++) {
newpikachu = pikachu.cloneNode(true);
portfolio.appendChild(newpikachu);
}

4.

var listItem = document.createElement('li');

var leftSpan = document.createElement('span');

var lastUpdated = document.createTextNode('Page last updated on');

leftSpan.appendChild(lastUpdated);

listItem.appendChild(leftSpan);

var dateText = document.createTextNode(new Date());

var rightSpan = document.createElement('span');

rightSpan.appendChild(dateText);

listItem.appendChild(rightSpan);

var bio = document.querySelector('aside > ul');

bio.appendChild(listItem);
