<%*
   let refnr = (await tp.system.suggester((item) => item.basename, app.vault.getMarkdownFiles())).basename
   const fooMeta = DataviewAPI.page(tp.file.find_tfile(refnr).path)
   let new_titel = tp.file.creation_date("YYYY-MM-DD_HHmm")
    tp.file.rename(new_titel)
   await tp.file.move("daily notes/" + tp.date.now("YYYY") +  "/" + tp.date.now("MM") + "/" + new_titel)
%>
type:: case_note
summary:: 
case_titel::<% fooMeta.titel %>
refnr:: [[<%refnr%>]]

### Methods

### Notes





