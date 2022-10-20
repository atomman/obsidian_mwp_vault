<%*
  let title = tp.file.title
  var output;
  if (title.startsWith("SAG-")) {
    output = await tp.file.include("[[templates/case note]]")
    await tp.file.rename(tp.file.title.slice(4))
  } else if (title.startsWith('LAB-')){
    output = await  tp.file.include("[[templates/lab notes]]")
    await tp.file.rename(tp.file.title.slice(4))
 } else if (title.startsWith('MØDE-')){
     output = await tp.file.include("[[templates/meeting]]")
     await tp.file.rename(tp.file.title.slice(5))
  } else {
    output = await tp.file.include("[[templates/daily note]]")
  }
%>

<%* tR +=`${output}` %>