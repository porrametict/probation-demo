<template>

    <v-container fluid>
        <v-card>
            <v-card-text>
                <h1 class="title">อ.ค.ป.๓ บันทึกผลการสอดส่อง(ระหว่างคุม/ฟื้นฟู)</h1>
                <v-form>
                    <v-row>
                        <v-col cols="12">
                            <v-text-field label="ครั้งที่"/>
                            <DatePicker/>
                            <v-text-field label="เลขทะเบียน"/>
                            <h1 class="subtitle-1">วันนี้ข้าพเจ้าได้ออกไปสอดส่องตามสถานที่อยู่เเจ้งไว้ ปรากฏว่า</h1>
                            <v-radio-group v-model="form.meet_radio" :mandatory="false">
                                <v-radio label="พบ ผู้ถูกคุมความประพฤติผู้เข้ารับการฟื้นฟูฯ" :value="true"></v-radio>
                                <v-radio label="ไม่พบ ผู้ถูกคุมความประพฤติผู้เข้ารับการฟื้นฟูฯ" :value="false"></v-radio>
                            </v-radio-group>

                            <div v-if="form.meet_radio === false">
                                <h1 class="subtitle-1">โดยสอบถามข้อมูล จาก</h1>
                                <v-text-field label="ชื่อ-สกุล"/>
                                <v-text-field label="เกี่ยวข้องเป็น"/>
                                <v-text-field label="อยู่บ้านเลขที่"/>
                                <v-text-field label="หมู่ที่"/>
                                <v-text-field label="ตรอก/ซอย"/>
                                <v-text-field label="ถนน"/>
                                <v-text-field label="ตำบล/เเขวง"/>
                                <v-text-field label="อำเภอ/เขต"/>
                                <v-text-field label="จังหวัด"/>
                                <v-text-field label="โทรศัพท์"/>
                            </div>
                        </v-col>
                    </v-row>
                </v-form>
            </v-card-text>
        </v-card>
    </v-container>
</template>

<script>
    import DatePicker from "./DatePicker";

    export default {
        name: 'HelloWorld',
        components: {DatePicker},
        data: () => ({
            form : {
                no : null,
                date : null,
                registration_number : null,
                meet_radio  : null


            }
        }),
    };
</script>
