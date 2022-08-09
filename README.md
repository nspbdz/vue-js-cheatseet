# vue-js-cheatseet
rules foto  tidak kosong dan max size 

 const sizeRules= [

              files => !files || !files.some(file => file.size > 2_097_152) || 'Size Foto KTP  Harus Di Bawah 2 MB!', v => !!v || 'Foto KTP Tidak Boleh Kosong'
            ]
            
        ##untuk upload foto
            
    const uploadPhotoKtp = (e) => {
        console.log(e.length);

        if(e.length !== 0){

        const file = e[0]
         urlKtp.value = URL.createObjectURL(file);
        const reader = new FileReader();
          reader.onloadend = function () {
          }

        reader.readAsDataURL(file);
        }else{

          console.log("kosong");
        }
          console.log(urlKtp);




      }

## untuk width sebuah halaman
 computed: {
      // eslint-disable-next-line vue/return-in-computed-property
      width() {
        switch (this.$vuetify.breakpoint.name) {
          case 'xs':
            return 320
          case 'sm':
            return 650
          case 'md':
            return 850
          case 'lg':
            return 1200
          case 'xl':
            return 1200
        }
      },
    },
