<!-- <template>
  <div class="container">
    <p>Upload {{ crop_name }} image to check if it is diseased or not</p>
    <div class="img_svg text-center mt-4">
        <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" fill="currentColor" class="bi bi-images" viewBox="0 0 16 16">
            <path d="M4.502 9a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3z"/>
            <path d="M14.002 13a2 2 0 0 1-2 2h-10a2 2 0 0 1-2-2V5A2 2 0 0 1 2 3a2 2 0 0 1 2-2h10a2 2 0 0 1 2 2v8a2 2 0 0 1-1.998 2zM14 2H4a1 1 0 0 0-1 1h9.002a2 2 0 0 1 2 2v7A1 1 0 0 0 15 11V3a1 1 0 0 0-1-1zM2.002 4a1 1 0 0 0-1 1v8l2.646-2.354a.5.5 0 0 1 .63-.062l2.66 1.773 3.71-3.71a.5.5 0 0 1 .577-.094l1.777 1.947V5a1 1 0 0 0-1-1h-10z"/>
        </svg>
    </div>
    <div class="form text-center">
        <form enctype="multipart/form-data">
        <input type="file" name="file" ref="inputFile" />
        <input type="submit" @click.prevent="Uploadfile" value="Upload" />
        </form>
    </div>



    <div class="l3tlg0-6 kkceuK">
    <button type="button" class="l3tlg0-0 ggoliT">
        <div class="sc-2xfn8l-0 bWaBkl sc-2wite4-0 itDlvX">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                <path d="M13 12v-2h1v2h2v1h-2v2h-1v-2h-2v-1h2zm5 8H6V4H5v17h13v-1zm1 0v2H4V3h2V1h10l5 5v14h-2zM7 2v17h13V6l-4-4H7zm9 0l4 4h-4V2z"></path>
            </svg>
        </div>
        <span class="sc-8s01yt-5 gGeCVP">Choose Files</span>
    </button>
    <button type="button" title="Expand menu" class="l3tlg0-2 gwHGeO">
        <div class="sc-1gyxcpm-0 hsyQfH" style="width:16px;height:16px">
            <svg viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" fill="currentColor">
                <path d="M13.3333 4L14.6666 5.33333L7.99992 12L1.33325 5.33333L2.66659 4L7.99992 9.5L13.3333 4Z"></path>
            </svg>
        </div>
    </button>
    </div> 



  </div>
</template> -->
<template>
  <div class="container text-center mt-4">
    <Navbar />
    <p>Upload {{ crop_name }} image to check if it is diseased or not</p>
    
    <div class="img_svg mt-4">
        <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" fill="currentColor" class="bi bi-images" viewBox="0 0 16 16">
            <path d="M4.502 9a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3z"/>
            <path d="M14.002 13a2 2 0 0 1-2 2h-10a2 2 0 0 1-2-2V5A2 2 0 0 1 2 3a2 2 0 0 1 2-2h10a2 2 0 0 1 2 2v8a2 2 0 0 1-1.998 2zM14 2H4a1 1 0 0 0-1 1h9.002a2 2 0 0 1 2 2v7A1 1 0 0 0 15 11V3a1 1 0 0 0-1-1zM2.002 4a1 1 0 0 0-1 1v8l2.646-2.354a.5.5 0 0 1 .63-.062l2.66 1.773 3.71-3.71a.5.5 0 0 1 .577-.094l1.777 1.947V5a1 1 0 0 0-1-1h-10z"/>
        </svg>
    </div><br>

    <form enctype="multipart/form-data">
        <input type="file" class="form-control" name="file" ref="inputFile" size="4"/>
        <button type="submit" class="form-control btn btn-info" @click.prevent="Uploadfile">Upload</button>
    </form>

  </div>
</template>

<script>
import router from '../router/index'
import Navbar from "../components/Navbar.vue"
export default {
    name: "Crop",
    components: {
        Navbar,
    },
    data() {
        return {
            crop_name: "",
        }
    },
    mounted() {
        this.crop_name = this.$route.params.crop_name;
        // console.log(this.crop_name);
    },
    methods: {
        async Uploadfile(event) {
            event.preventDefault()
            let formData = new FormData();
            // console.log(this.$refs.inputFile);
            formData.append('file', this.$refs.inputFile.files[0]);
            // axios.post('/upload/' + this.crop_name, formData)
            // let response = fetch(`http://127.0.0.1:5000/upload/${this.crop_name}`, {
            //     method: 'POST',
            //     body: formData
            // })
            const response = await fetch("http://127.0.0.1:5000/upload", {
                method: 'POST',
                body: formData
            })
            if (response.ok) {
                const data = await response.json();
                console.log('File uploaded successfully');
                alert("File uploaded successfully")
                router.push({ 
                    name: 'Result',
                    query: { 
                        class_label: data.class_label,
                        confidence: data.confidence,
                        total_spots: data.total_spots
                    }
                });
            } else {
                console.error('Error uploading file')
            }
            
        }
    },

}
</script>

<style scoped>
form {
    display: flex;
    align-content: center;
    align-items: center;
}
</style>