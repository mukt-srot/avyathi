<script>
    import { fade } from 'svelte/transition';
    import { states } from "./States.js";
    let placeholder = "Select your state here";
    let selected;
    let submitted = false;

    function handleSubmit(event) {
        event.preventDefault();
        submitted = true;
    }

    function handleStateChange(event) {
        selectedState = event.target.value;
    }

    let naam = "";
    let email = "";
    let selectedState = "";

    // Styles
    const btnStyle = "text-warmGray-900 bg-cyan-100 hover:bg-cyan-400 focus:ring-4 focus:outline-none focus:ring-cyan-200 font-medium rounded-lg text-md px-3 py-1 text-center mr-3";
    const linkStyle = "text-red-900"
</script>

<main class="transition:fade={{ delay: 300, duration: 400 }}">
    <div class="flex items-center justify-center">
    <div class="max-w-sm p-6 bg-lime-200 shadow-lg rounded-lg my-4">
        <div class="flex text-center justify-center ">
        <!-- Form -->
        <form on:submit={handleSubmit}>
            <div class="mb-2 font-medium opacity-80">
                <!-- Name and email input field -->
                <label>
                    Name <input
                        bind:value={naam}
                        placeholder=" Enter your name here" class="rounded-lg outline-none"/>
                </label><br /><br />
                <label>
                    Email &nbsp;
                    <input
                      {email} 
                      placeholder="Enter your email here (optional)"
                      type="email" 
                      class="rounded-lg outline-none"
                    />
                  </label>
                  
            </div>

            <br />

            <div class="mx-8">
                <select bind:value={selected} on:change={handleStateChange} class="rounded-md p-1 w-60 outline-none opacity-80">
                    <option value={placeholder} disabled selected
                        >{placeholder}</option
                    >
                    {#each states as state}
                        <option value={state}>{state.name}</option>
                    {/each}
                </select>
            </div>
            <br />
            <button disabled={!selected} type="submit" class={btnStyle}
                >Submit</button
            >
        </form>
    
    </div>
</div>
</div>
{#if !submitted}
    <div class="flex items-center justify-center my-6">
    <div class="flex flex-col items-center bg-lime-200 rounded-lg shadow-lg md:flex-col md:max-w-4xl p-2" transition:fade={{ delay: 300, duration: 400 }}>
        <p class="p-1">
            Enter your details above. Your Name and details are encrypted (Even we won't be able to see it). <a href="https://github.com/mukt-srot/avyathi" target="_blank" class={linkStyle}>Avyathi</a> is an open-source project committed to tackling the rising issue of digital crimes, especially the growing threat of deepfake technology. 
        </p>
        <p class="p-1"> 
            Our primary objective is to provide a comprehensive directory of respective cyber-police cells to aid individuals in reporting incidents related to deepfake crimes. Additionally, we will offer valuable insights and tips on gathering evidence, preserving digital footprints, and understanding the nuances of deepfake technology during the complaint process.
            
        </p> 
        <p class="p-1">     
            Your personal information remains encrypted, ensuring that even our team cannot access or view your details. We value your trust in our platform and prioritize the safeguarding of your data.
        </p>
    </div>
    </div>

{/if}

{#if submitted}
{#each states as state}
    {#if state === selected}
    <p class="justify-center text-center">Here's the directory for {state.name} Police 👇</p>
    <div class="flex items-center justify-center my-4">
        <div class="flex flex-col items-center bg-lime-200 rounded-lg shadow-lg md:flex-row md:max-w-4xl p-2">
            <p class="p-1">👉 Have screenshots and evidence of the photo and chats. Also export chats if possible.<br><br> 

            👉 Register your complaint in <a href="https://cybercrime.gov.in/" target="_blank" class={linkStyle}>Govt of India Cyber Crime Portal</a>. <br><br>
                
            👉 You can DM the cyber-cell twitter handle of your state(if it has)  and make sure to mention your contact details there.
            </p><br>
            <p class="p-1">
                👉 State: {state.name} <br>
                👉 Police Website: <a href={state.website} target="_blank" class={linkStyle}>{state.website}</a> <br>
                👉 Police Twitter Handle: <a href={state.twitter} target="_blank" class={linkStyle}>{state.twitter}</a> <br>
                👉 National Cyber Complaint Portal : <a href="https://cybercrime.gov.in/" target="_blank" class={linkStyle}>https://cybercrime.gov.in/</a><br>
                👉<a href="https://www.rbi.org.in/commonman/Upload/English/Content/PDFs/LNA100112C_M.pdf" class={linkStyle}>List of Nodal Agencies (Cyber Crime Cells) in India</a>
            </p>
        </div>
    </div>    
    {/if}
{/each}
{/if}

</main>

