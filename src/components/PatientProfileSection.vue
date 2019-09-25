<template>
  <div class="card">
    <div class="card-content">
      <b-field grouped>
        <b-field
          label="เลขที่บัตรประจำตัวประชาชน : "
          expanded
          type="is-danger"
          message="(ใส่เฉพาะตัวเลข 0-9 เท่านั้น)"
        >
          <b-input v-model="patientProfile.citizenId" placeholder="เลขที่บัตรประจำตัวประชาชน" rounded></b-input>
        </b-field>
      </b-field>
      <b-field grouped>
        <b-field label="คำนำหน้า">
          <b-select v-model="patientProfile.title">
            <option>นาย</option>
            <option>นาง</option>
            <option>นางสาว</option>
          </b-select>
        </b-field>
        <b-field label="ชื่อ" expanded>
          <b-input v-model="patientProfile.firstName" placeholder="ชื่อ" rounded></b-input>
        </b-field>
        <b-field label="นามสกุล" expanded>
          <b-input v-model="patientProfile.lastName" placeholder="นามสกุล" rounded></b-input>
        </b-field>
      </b-field>
      <b-field grouped>
        <b-field label="วัน/เดือน/ปีเกิด">
            <b-datepicker v-model="patientProfile.birthday"
                placeholder="โปรดเลือก..."
                icon="calendar-today">
            </b-datepicker>
        </b-field>
        <b-field label="ศาสนา">
          <b-select v-model="patientProfile.religious">
            <option>พุทธ</option>
            <option>อิสลาม</option>
            <option>คริสต์</option>
            <option>ฮินดู</option>
            <option>ซิกซ์</option>
            <option>อื่นๆ</option>
            <option>ไม่ระบุ</option>
          </b-select>
        </b-field>
        <b-field label="เชื่อชาติ" expanded>
          <b-input v-model="patientProfile.ethnicity" placeholder="เชื่อชาติ" rounded></b-input>
        </b-field>
        <b-field label="สัญชาติ" expanded>
          <b-input v-model="patientProfile.nationality" placeholder="สัญชาติ" rounded></b-input>
        </b-field>
      </b-field>
      <p>{{ patientProfile }}</p>
    </div>
  </div>
</template>
<script>
export default {
  data: function() {
    return {
      patientProfile: {
        citizenId: 0,
        prefix: "",
        firstName: "",
        lastName: "",
        birthday: "",
        religious: "",
        ethnicity: "",
        nationality: "",
      }
    };
  }
};
</script>