# Assessments & Results Portal

Complete evaluation materials including weekly tests, class tests, preliminary exams, and **your assessment results**.

---

## 🎓 View Your Scorecard

Enter your details to access your personalized assessment results:

<div style="max-width: 500px; margin: 2rem auto; padding: 2rem; background: #f8f9fa; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.08);">

  <form id="scorecardForm" style="display: flex; flex-direction: column; gap: 1.2rem;">
    
    <div>
      <label for="firstName" style="display: block; margin-bottom: 0.5rem; font-weight: 600; color: #003366;">First Name</label>
      <input type="text" id="firstName" placeholder="e.g., Akash" required style="width: 100%; padding: 0.75rem; border: 2px solid #ddd; border-radius: 4px; font-size: 1rem; transition: border-color 0.3s; box-sizing: border-box;" />
    </div>

    <div>
      <label for="lastName" style="display: block; margin-bottom: 0.5rem; font-weight: 600; color: #003366;">Last Name / Surname</label>
      <input type="text" id="lastName" placeholder="e.g., Chatake" required style="width: 100%; padding: 0.75rem; border: 2px solid #ddd; border-radius: 4px; font-size: 1rem; transition: border-color 0.3s; box-sizing: border-box;" />
    </div>

    <div>
      <label for="rollNumber" style="display: block; margin-bottom: 0.5rem; font-weight: 600; color: #003366;">Roll Number</label>
      <input type="number" id="rollNumber" placeholder="e.g., 3201" required style="width: 100%; padding: 0.75rem; border: 2px solid #ddd; border-radius: 4px; font-size: 1rem; transition: border-color 0.3s; box-sizing: border-box;" />
    </div>

    <button type="submit" style="padding: 0.9rem 1.5rem; background: linear-gradient(90deg, #003366 0%, #0055a5 100%); color: white; border: none; border-radius: 4px; font-size: 1rem; font-weight: 600; cursor: pointer; transition: transform 0.2s, box-shadow 0.2s;" onmouseover="this.style.transform='translateY(-2px)'; this.style.boxShadow='0 4px 12px rgba(0,51,102,0.3)';" onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='none';">
      View My Scorecard
    </button>

  </form>

  <div id="message" style="margin-top: 1rem; padding: 0.75rem; border-radius: 4px; display: none; text-align: center; font-weight: 500;"></div>

</div>

---

## 📋 Assessment Structure

### Weekly Tests (5 Papers)
**Duration:** 1 hour each  
**Format:** Multiple choice + Short answers  
**Coverage:** Individual unit concepts

- **WT1:** Unit 1 Foundations
- **WT2:** Unit 2 Supervised Learning
- **WT3:** Unit 3 Unsupervised Learning
- **WT4:** Unit 4 Advanced Topics
- **WT5:** Unit 5 Ethics & Production

---

### Class Tests (2 Papers)
**Duration:** 2 hours each  
**Format:** Mixed (MCQ + Short + Long answers)  
**Coverage:** 2-3 units per test

- **CT1:** Units 1-2
- **CT2:** Units 3-4

---

### Preliminary Exams (2 Papers)
**Duration:** 3 hours each  
**Format:** Comprehensive (all question types)  
**Coverage:** Entire curriculum

- **Prelim 1:** Full course paper
- **Prelim 2:** Full course paper (alternative)

---

## Resources

- **Question Banks:** Extensive practice questions
- **Answer Keys:** Complete solutions
- **Marking Schemes:** Official MSBTE guidelines
- **Model Answers:** Reference responses

---

## How to Use Assessments

1. **Self-Assessment:** Check your understanding before tests
2. **Practice:** Prepare for actual exams
3. **Evaluation:** Formal assessment after completion
4. **Review:** Learn from mistakes and improve

---

<script>
// Client-side SHA-256 hashing for secure scorecard access
async function hashScorecardKey(firstName, lastName, rollNumber) {
  // Clean inputs: trim whitespace, convert to lowercase
  const first = firstName.trim().toLowerCase();
  const last = lastName.trim().toLowerCase();
  const roll = String(rollNumber).trim();
  
  // Extract first 2 letters of first name, first 2 letters of last name, append roll
  const key = first.substring(0, 2) + last.substring(0, 2) + roll;
  
  // Encode as UTF-8 and hash with SHA-256
  const encoder = new TextEncoder();
  const data = encoder.encode(key);
  const hashBuffer = await crypto.subtle.digest('SHA-256', data);
  
  // Convert ArrayBuffer to hex string
  const hashArray = Array.from(new Uint8Array(hashBuffer));
  const hashHex = hashArray.map(byte => byte.toString(16).padStart(2, '0')).join('');
  
  return hashHex;
}

// Form submission handler
document.getElementById('scorecardForm').addEventListener('submit', async function(e) {
  e.preventDefault();
  
  const firstName = document.getElementById('firstName').value;
  const lastName = document.getElementById('lastName').value;
  const rollNumber = document.getElementById('rollNumber').value;
  const messageDiv = document.getElementById('message');
  
  // Validation
  if (!firstName.trim() || !lastName.trim() || !rollNumber.trim()) {
    messageDiv.textContent = '❌ Please fill in all fields';
    messageDiv.style.backgroundColor = '#f8d7da';
    messageDiv.style.color = '#721c24';
    messageDiv.style.display = 'block';
    return;
  }
  
  if (isNaN(rollNumber) || parseInt(rollNumber) <= 0) {
    messageDiv.textContent = '❌ Roll number must be a valid number';
    messageDiv.style.backgroundColor = '#f8d7da';
    messageDiv.style.color = '#721c24';
    messageDiv.style.display = 'block';
    return;
  }
  
  try {
    messageDiv.textContent = '⏳ Loading your scorecard...';
    messageDiv.style.backgroundColor = '#cfe2ff';
    messageDiv.style.color = '#084298';
    messageDiv.style.display = 'block';
    
    // Generate hash
    const hash = await hashScorecardKey(firstName, lastName, rollNumber);
    
    // Redirect to results page with hashed filename
    window.location.href = `/ml-site/results/${hash}.html`;
    
  } catch (error) {
    console.error('Error:', error);
    messageDiv.textContent = '❌ An error occurred. Please try again.';
    messageDiv.style.backgroundColor = '#f8d7da';
    messageDiv.style.color = '#721c24';
    messageDiv.style.display = 'block';
  }
});

// Example: Log the hash for debugging (remove in production)
// Uncomment the line below and enter details to see the generated hash
console.log('Hash function ready. Format: firstNameInitials(2) + lastNameInitials(2) + rollNumber → SHA-256');
</script>

<style>
#firstName:focus, #lastName:focus, #rollNumber:focus {
  border-color: #0055a5 !important;
  outline: none;
  box-shadow: 0 0 0 3px rgba(0, 85, 165, 0.1);
}

#scorecardForm button:disabled {
  opacity: 0.6;
  cursor: not-allowed;
}
</style>

---

[Back to Home](../)
