<%*
  let title = tp.file.title
  var output;
  if (title.startsWith("CASE-")) {
    output = await tp.file.include("[[case]]")
    await tp.file.rename(tp.file.title.slice(4))
  } else if (title.startsWith('LAB-')){
    output = await  tp.file.include("[[case note]]")
    await tp.file.rename(tp.file.title.slice(4))
 } else if (title.startsWith('MEETING-')){
     output = await tp.file.include("[[templates/meeting]]")
     await tp.file.rename(tp.file.title.slice(5))
  } else {
    output = await tp.file.include("[[templates/case note]]")
  }
%>

<%* tR +=`${output}` %>