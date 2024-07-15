<template>
  <ckeditor :editor="editor" v-model="editorData" :config="editorConfig"></ckeditor>
</template>

<script>
import { ClassicEditor, Bold, Essentials, Italic, Mention, Paragraph, Undo, Heading, BlockQuote, Font, Link, List } from 'ckeditor5';

import 'ckeditor5/ckeditor5.css';

export default {
  name: 'app',
  data() {
    return {
      editor: ClassicEditor,
      editorData: '<p>Hello from CKEditor 5 in Vue!</p>',
      editorConfig: {
        plugins: [Bold, Essentials, Italic, Mention, Paragraph, Undo, Heading, BlockQuote, Font, Link, List],
        toolbar: ['heading',
          '|',
          'bold',
          'italic',
          'fontSize',
          'fontFamily',
          'fontColor',
          '|',
          'link',
          'bulletedList',
          'numberedList',
          'blockQuote'],
        licenseKey: '<YOUR_LICENSE_KEY>',
        mention: {
          // Mention configuration
        },
      },
    };
  }
}
</script>
