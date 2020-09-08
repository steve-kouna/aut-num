<template>
  <div>
    <form class="form" @submit.prevent="handleSubmit">
      <label for="">
        Aut num
        <input
          type="text" 
          v-model="attributes.aut_num"
        >
      </label>
      <br><br>
      <label for="">
        as_name
        <input
          type="text" 
          v-model="attributes.as_name"
        >
      </label>
      <br><br>
      <label for="">
        descr
        <textarea
          v-model="attributes.descr"
        ></textarea>
      </label>
      <br><br>
      <label for="">
        status
        <select v-model="attributes.status">
          <option
            v-for="statu in status"
            v-bind:value="statu.value"
            :key="statu.value"
          >
            {{ statu.text }}
          </option>
        </select>
      </label>
      <br><br>
      <label for="">
        member_of
        <input
          type="text" 
          v-model="attributes.member_of"
        >
      </label>
      <br><br>
      <label for="">
        import
        <input
          type="text" 
          v-model="attributes.import"
        >
      </label>
      <br><br>
      <label for="">
        mp_import
        <input
          type="text" 
          v-model="attributes.mp_import"
        >
      </label>
      <br><br>
      <label for="">
        default
        <input
          type="text" 
          v-model="attributes.default"
        >
      </label>
      <br><br>
      <label for="">
        mp_default
        <input
          type="text" 
          v-model="attributes.mp_default"
        >
      </label>
      <br><br>
      <label for="">
        remarks
        <input
          type="text" 
          v-model="attributes.remarks"
        >
      </label>
      <br><br>
      <label for="">
        org
        <input
          type="text" 
          v-model="attributes.org"
        >
      </label>
      <br><br>
      <label for="">
        admin_c
        <input
          type="text" 
          v-model="attributes.admin_c"
        >
      </label>
      <br><br>
      <label for="">
        tech_c
        <input
          type="text" 
          v-model="attributes.tech_c"
        >
      </label>
      <br><br>
      <label for="">
        notify
        <input
          type="text" 
          v-model="attributes.notify"
        >
      </label>
      <br><br>
      <label for="">
        mnt_irt
        <input
          type="text" 
          v-model="attributes.mnt_irt"
        >
      </label>
      <br><br>
      <label for="">
        mnt_lower
        <input
          type="text" 
          v-model="attributes.mnt_lower"
        >
      </label>
      <br><br>
      <label for="">
        mnt_routes
        <input
          type="text" 
          v-model="attributes.mnt_routes"
        >
      </label>
      <br><br>
      <label for="">
        mnt_by
        <input
          type="text" 
          v-model="attributes.mnt_by"
        >
      </label>
      <br><br>
      <label for="">
        changed
        <input
          type="text" 
          v-model="attributes.changed"
        >
      </label>
      <br><br>
      <label for="">
        source
        <input
          type="text" 
          v-model="attributes.source"
        >
      </label>

      <br><br>
      <button type="submit">Save</button>
    </form>
  </div>
</template>

<script>

export default {
  name: 'AutNumForm',
  data () {
    return{
      status: [
        { text: 'ASSIGNED', value: 'ASSIGNED' },
        { text: 'AFPUB-2004-ASN-001', value: 'AFPUB-2004-ASN-001' },
        { text: 'ASSIGNED-ANYCAST', value: 'ASSIGNED-ANYCAST' },
        { text: 'AFPUB-2012-V4-001', value: 'AFPUB-2012-V4-001' },
        { text: 'POLICY-RESERVED', value: 'POLICY-RESERVED' },
        { text: 'AFPUB-2014-GEN-004', value: 'AFPUB-2014-GEN-004' },
      ],
      attributes: {
        aut_num: '',
        as_name: '',
        descr: '',
        status: '',
        member_of: '',
        import: '',
        mp_import: '',
        export: '',
        mp_export: '',
        default: '',
        mp_default: '',
        remarks: '',
        org: '',
        admin_c: '',
        tech_c: '',
        notify: '',
        mnt_irt: '',
        mnt_lower: '',
        mnt_routes: '',
        mnt_by: '',
        changed: '',
        source: ''
      },
    };
  },

  mounted() {
    const date = new Date();
    const timestamp = date.getTime();
    this.attributes.aut_num = 'An-' + timestamp;
  },

  methods: {
    handleSubmit() {
      console.log(this.attributes);
    },
  },
}
</script>

