---
title: "Contact"
description: "Raleigh Durham Chapel Hill North Carolina Sleep Consultant Pediatric Dietitian Nutritionist"
layout: simple
keywords:
- "nutrition"
- "counseling"
- "dietitian"
- "nutritionist"
- "sleep"
- "coach"
- "consultant"
- "child"
- "pediatric"
- "chapel hill"
- "raleigh"
- "durham"
- "north carolina"
---
<div class="flex items-center min-h-screen bg-gray-100 dark:bg-gray-900">
  <div class="container mx-auto">
    <div class="max-w-xl mx-auto my-10 bg-white p-5 rounded-md shadow-sm">
      <div class="text-center">
        <p class="text-gray-400 dark:text-gray-400">
          Fill up the form below to send me a message.
        </p>
      </div>
      <div class="m-7">
        <form netlify validate name="contact" method="POST onSubmit={handleSubmit}">
          <input type="hidden" name="contact" value="contact">
          <input type="checkbox" name="botcheck" id="" style="display: none;" />
          <div class="flex mb-6 space-x-4">
            <div class="w-full md:w-1/2">
              <label for="fname" class="block mb-2 text-sm text-gray-600 dark:text-gray-400">First Name</label>
              <input type="text" name="first_name" id="fname" placeholder="John" required class="w-full px-3 py-2 placeholder-gray-300 border-2 border-gray-200 rounded-md focus:outline-none focus:ring focus:ring-indigo-100 focus:border-indigo-300" oninvalid="this.setCustomValidity('Please enter your first name.')" onkeyup="setCustomValidity('')"/>
            </div>
            <div class="w-full md:w-1/2">
              <label for="lname" class="block mb-2 text-sm text-gray-600 dark:text-gray-400">Last Name</label>
              <input type="text" name="last_name" id="lname" placeholder="Doe" required class="w-full px-3 py-2 placeholder-gray-300 border-2 border-gray-200 rounded-md focus:outline-none focus:ring focus:ring-indigo-100 focus:border-indigo-300" oninvalid="this.setCustomValidity('Please enter your last name.')" onkeyup="setCustomValidity('')"/>
            </div>
          </div>
          <div class="flex mb-6 space-x-4">
            <div class="w-full md:w-1/2">
              <label for="email" class="block mb-2 text-sm text-gray-600 dark:text-gray-400">Email Address</label>
              <input type="email" name="email" id="email" placeholder="you@company.com" required class="w-full px-3 py-2 placeholder-gray-300 border-2 border-gray-200 rounded-md focus:outline-none focus:ring focus:ring-indigo-100 focus:border-indigo-300" oninvalid="this.setCustomValidity('Please enter a valid email address.')" onkeyup="setCustomValidity('')"/>
            </div>
            <div class="w-full md:w-1/2">
              <label for="phone" class="block text-sm mb-2 text-gray-600 dark:text-gray-400">Phone Number</label>
              <input type="text" name="phone" id="phone" placeholder="+1 (555) 1234-567" required class="w-full px-3 py-2 placeholder-gray-300 border-2 border-gray-200 rounded-md focus:outline-none focus:ring focus:ring-indigo-100 focus:border-indigo-300" oninvalid="this.setCustomValidity('Please enter your phone number.')" onkeyup="setCustomValidity('')"/>
            </div>
          </div>
          <div class="mb-6">
            <label for="prefer" class="block mb-2 text-sm text-gray-600 dark:text-gray-400">How do you prefer to be contacted?</label>
            <select name="prefer" id="prefer" class="w-full px-3 py-2" required>
              <option value="">--Please choose an option--</option>
              <option>Email</option>
              <option>Phone</option>
              <option>Text</option>
            </select>
          </div>
          <div class="mb-6">
            <label for="what" class="block mb-2 text-sm text-gray-600 dark:text-gray-400">Interested in</label>
            <select name="what" id="what" class="w-full px-3 py-2" required>
              <option value="">--Please choose an option--</option>
              <option>Nutrition Counseling</option>
              <option>Sleep Consulting</option>
              <option>Speaking</option>
              <option>Press</option>
              <option>General Inquiry</option>
            </select>
          </div>
          <div class="mb-6">
            <label for="how_hear" class="block mb-2 text-sm text-gray-600 dark:text-gray-400">How did you hear about me? (optional)</label>
            <input type="text" name="how_hear" id="how_hear" placeholder="" class="w-full px-3 py-2 placeholder-gray-300 border-2 border-gray-200 rounded-md focus:outline-none focus:ring focus:ring-indigo-100 focus:border-indigo-300"></textarea>
          </div>
          <div class="mb-6">
            <label for="message" class="block mb-2 text-sm text-gray-600 dark:text-gray-400">Your Message</label>
            <textarea rows="5" name="message" id="message" placeholder="Your Message" class="w-full px-3 py-2 placeholder-gray-300 border-2 border-gray-200 rounded-md focus:outline-none focus:ring focus:ring-indigo-100 focus:border-indigo-300" required oninvalid="this.setCustomValidity('Please enter your message.')" onkeyup="setCustomValidity('')"></textarea>
            <div class="empty-feedback invalid-feedback text-red-400 text-sm mt-1">
              Please enter your message.
            </div>
          </div>
          <div class="mb-6">
            <button type="submit" class="w-full px-3 py-4 text-white bg-indigo-500 rounded-md focus:bg-indigo-600 focus:outline-none">
              Send Message
            </button>
          </div>
          <p class="text-base text-center text-gray-400" id="result"></p>
        </form>
      </div>
    </div>
  </div>
</div>

<script>
const handleSubmit = (event) => {
  event.preventDefault();

  const myForm = event.target;
  const formData = new FormData(myForm);
  
  fetch("/", {
    method: "POST",
    headers: { "Content-Type": "application/x-www-form-urlencoded" },
    body: new URLSearchParams(formData).toString(),
  })
    .then(() => alert("Thank you for your submission, I will be in touch."))
    .catch((error) => alert(error));
};

document
  .querySelector("form")
  .addEventListener("submit", handleSubmit);

</script>

**Call/text**: 919-809-5452

{{< button href="https://app.simplymeet.me/gretabreskin">}}
Book a Discovery Call
{{< /button >}}