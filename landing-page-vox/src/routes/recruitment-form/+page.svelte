<script>
    //export form data to a json file
    import { onMount } from 'svelte';
    import { page } from '$app/stores';

    onMount(() => {
        const form = document.querySelector('form');
        form.addEventListener('submit', (e) => {
            e.preventDefault();
            const formData = new FormData(form);
            const data = Object.fromEntries(formData);
            console.log(data);
            fetch('/api/recruitment-form', {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json'
                },
                body: JSON.stringify(data)
            }).then(() => {
                window.location.href = $page.document + '/success';
            });
        });
    });


    //make a map for the radio buttons with the labels as objects
    const selectLabels = [{
        label: "Programming (Code, Frontend, Backend, Full Stack, App Dev)",
        value: "Programming (Code, Frontend, Backend, Full Stack, App Dev)"
    }, {
        label: "Communication (People Skills, Team Management, Presentation)",
        value: "Communication (People Skills, Team Management, Presentation)"
    }, {
        label: "Technical (Problem Solving, System Design)",
        value: "Technical (Problem Solving, System Design)"
    }, {
        label: "Designing (UI/UX, Graphic Design, Brand Design, Social Post Design)",
        value: "Designing (UI/UX, Graphic Design, Brand Design, Social Post Design)"
    }];

    let selectedOption = selectLabels[0].value;

    function handleSelectChange(event) {
        selectedOption = event.target.value;
    }

    let phoneNumber = '';

    const handlePhoneInput = (event) => {
        const inputValue = event.target.value;
        const numericValue = inputValue.replace(/\D/g, ''); // Remove non-numeric characters
        phoneNumber = numericValue;
    };

    let email = '';

  function handleEmailInput(event) {
    email = event.target.value;
  }

  function emailIsValid(email) {
    // Use a regular expression to validate the email format
    const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
    return emailRegex.test(email);
  }

    const handleSubmit = () => {
        if (!emailIsValid(email)) {
            alert('Please enter a valid email address.');
            return;
        }
  };

</script>

<style>
    @import '../../font-import.css';
    @import '../recruitment-form/form.css';

    p{
        margin: 0%;
        color: #deeab8cf;
    }
</style>

<body>
    <div style="height: 50px"></div>
    <div class="form-pad">
        <form method="POST" on:submit|preventDefault={handleSubmit}>
            <h3>So you're interested...</h3>
            <p>Answer some questions about yourself now and we'll reach out to you based on your response.</p><br>
            
            <label for="name">Name:*</label>
            <input type="text" id="name" name="name" required><br>
            
            <label for="email">Email:*</label>
            <input type="text" id="email" name="email" on:submit|preventDefault ={handleEmailInput} required><br>

            <label for="phone">Phone:*</label>
            <p class="secondary-text">Preferably your WhatsApp number</p>
            <input type="text" id="phone" name="phone" value={phoneNumber} on:input={handlePhoneInput} required><br>

            <label for="techpassion">Are you passionate about any topic related to the Computer Industry? If so, tell us about it shortly:</label>
            <input type="text" id="techpassion" name="techpassion" required><br>

            <label for="techskills">What technical skills do you have?:</label><br>
            <select value={selectedOption} on:change={handleSelectChange}>
                {#each selectLabels as selectLabel}
                    <option value={selectLabel.value}>{selectLabel.label}</option>
                {/each}  
            </select><br>

            <label for="projectportfolio">Enter the link to your Project Portfolio</label>
            <p class="secondary-text">via Google Drive, Linktree or Personal Website. This is to make sure you'll be committed to our community a 100%.</p>
            <input type="text" id="projectportfolio" name="projectportfolio" required><br>
            <button class="form-submit-button">Submit</button>  
        </form>
        
    </div>
    
    <hr/>
</body>