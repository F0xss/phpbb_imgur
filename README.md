# phpbb_imgur
Interface for phpbb forums to upload images on imgur

#installation

1. Create folder "imgur" in your forum directory (For example .../forum/imgur). Copy files to this folder.
2. Register on imgur.com
3. Create new application. Select "OAuth 2 autorization with a callback url", callback url set to imgurredirect.php. Get Client Id and Client secret.
4. Modify imgur.js, set clientId and clientSecret.
5. Modify forum files (for prosilver2 theme):
  .../forum/styles/prosilver.mod2/template/posting_buttons.html
    after:
      <script type="text/javascript" src="{T_SUPER_TEMPLATE_PATH}/editor.js"></script>
    add:
      <link href="{ROOT_PATH}imgur/imgur.css" type=text/css rel=stylesheet>
      <script type="text/javascript" src="{ROOT_PATH}imgur/imgur.js"></script>

    after:
      <button type="button" accesskey="y" onclick="insert_listitem()" title="{L_BBCODE_LISTITEM_HELP}">[*]</button>
    add:
      <button type="button" onclick="UploadToImgurWindow(event)" title="{L_BBCODE_P_HELP}">Imgur</button>
6. Now you hav "imgur" button to upload images to imgur.com from your phpbb forum.

<img src="http://i.imgur.com/mDpgGIr.jpg">
