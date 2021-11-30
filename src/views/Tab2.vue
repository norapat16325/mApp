<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>สินค้า</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-grid>
        <ion-row>
          <ion-col>
            <ion-card>
              <ion-card-header>
                <ion-card-title> สินค้า 1 </ion-card-title>
                </ion-card-header>
                <ion-card-content>
                  รายละเอียด สินค้า 1
                  </ion-card-content>
                  <ion-card-content>
                <ion-button color="success" size="small" @click="buy"> สั่งซื้อ </ion-button>
                </ion-card-content>
              </ion-card>
            </ion-col>

            <ion-col>
            <ion-card>
              <ion-card-header>
                <ion-card-title> สินค้า 2 </ion-card-title>
                </ion-card-header>
                <ion-card-content>
                  รายละเอียด สินค้า 2
                  </ion-card-content>
                  <ion-card-content>
                <ion-button color="success" size="small" @click="buy"> สั่งซื้อ </ion-button>
                </ion-card-content>
              </ion-card>
            </ion-col>
         </ion-row>
         <ion-row>
            <ion-col>
            <ion-card>
              <ion-card-header>
                <ion-card-title> สินค้า 3 </ion-card-title>
                </ion-card-header>
                <ion-card-content>
                  รายละเอียด สินค้า 3
                  </ion-card-content>
                  <ion-card-content>
                <ion-button color="success" size="small" @click="buy"> สั่งซื้อ </ion-button>
                </ion-card-content>
              </ion-card>
            </ion-col>
             <ion-col>
            <ion-card>
              <ion-card-header>
                <ion-card-title> สินค้า 4 </ion-card-title>
                </ion-card-header>
                <ion-card-content>
                  รายละเอียด สินค้า 4
                  </ion-card-content>
                  <ion-card-content>
                <ion-button color="success" size="small" @click="buy"> สั่งซื้อ </ion-button>
                </ion-card-content>
              </ion-card>
            </ion-col>
         </ion-row>
         <ion-row>
           <ion-col>
            <ion-card>
              <ion-card-header>
                <ion-card-title> สินค้า 5 </ion-card-title>
                </ion-card-header>
                <ion-card-content>
                  รายละเอียด สินค้า 5
                  </ion-card-content>
                  <ion-card-content>
                <ion-button color="success" size="small" @click="buy"> สั่งซื้อ </ion-button>
                </ion-card-content>
              </ion-card>
            </ion-col>
            <ion-col>
            <ion-card>
              <ion-card-header>
                <ion-card-title> สินค้า 6 </ion-card-title>
                </ion-card-header>
                <ion-card-content>
                  รายละเอียด สินค้า 6
                  </ion-card-content>
                  <ion-card-content>
                <ion-button color="success" size="small" @click="buy"> สั่งซื้อ </ion-button>
                </ion-card-content>
              </ion-card>
            </ion-col>
         </ion-row>
      </ion-grid>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import {  alertController, IonButton, IonCard, IonCardHeader, IonCardTitle, IonCardContent, IonPage, IonHeader, IonToolbar, IonTitle, IonContent,  IonGrid, IonRow, IonCol } from '@ionic/vue';

export default  {
  name: 'Tab2',
  components: { IonButton,IonCard, IonCardHeader, IonCardTitle, IonCardContent,IonHeader, IonToolbar, IonTitle, IonContent, IonPage,  IonGrid, IonRow, IonCol },

methods :{
  async buy(){
    const alert = await alertController.create({
      message: "ยืนยันการสั่งซื้อ $(id)",
      buttons: [
        {
          text: "ยืนยัน",
          handler: () => {
            console.log("ยืนยัน");
            
          }
        },

        {
          text: "ยกเลิก",
           handler: () =>{
             console.log("ยกเลิก");
           }
          
        }
      ]
    });
    await alert.present();
  }
}
};
</script>