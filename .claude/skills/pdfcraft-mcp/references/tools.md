# PdfCraft tool catalogue

A snapshot of `crates/automation/src/tools.rs` (161 tools), grouped by name prefix. It can lag behind the code: `tools/list`, `tool_search` or `pdfcraft-cli tools` give the current set and each tool's full `input_schema`.

Flags: **RO** read-only, **destructive** removes content or overwrites files. *Command* is the app registry id the tool automates (usable with `command_run`).

## Documents

| Tool | What it does | Flags | Command |
|---|---|---|---|
| `doc_open` | Open a PDF |  | `file.open` |
| `doc_list` | List open documents | RO |  |
| `doc_info` | Inspect a document | RO | `file.properties` |
| `doc_close` | Close a document |  | `file.close` |
| `doc_save` | Save a document | destructive | `file.save` |
| `doc_set_info` | Set document metadata |  |  |
| `doc_combine` | Combine files |  | `page.combine` |
| `doc_create_multiple` | Create PDF from multiple files |  | `create.multiple` |
| `doc_split` | Split a document |  | `page.split` |
| `doc_export_data` | Export comments or form data | destructive |  |
| `doc_import_data` | Import comments or form data |  |  |
| `doc_hidden_info` | Find hidden information | RO |  |
| `doc_remove_hidden` | Remove hidden information / Sanitize | destructive |  |
| `doc_audit_redactions` | Audit faux redactions | RO |  |
| `doc_print` | Print |  |  |
| `doc_protect` | Protect with passwords |  | `protect.password` |
| `doc_unprotect` | Remove security | destructive | `protect.remove` |
| `doc_header_footer` | Add header and footer |  | `edit.header_footer` |
| `doc_watermark` | Add watermark |  | `edit.watermark` |
| `doc_background` | Add background |  | `edit.background` |
| `doc_remove_marks` | Remove header & footer, watermark or background | destructive |  |
| `doc_export_images` | Export pages as images |  | `export.image` |
| `doc_export_office` | Export to Word, PowerPoint, HTML or RTF |  | `export.docx` |
| `doc_compare` | Compare files | RO | `doc.compare` |
| `doc_compare_report` | Compare report |  | `doc.compare` |
| `doc_compare_mark` | Mark differences as comments |  | `doc.compare` |
| `doc_export_all_images` | Export all images |  | `export.all_images` |
| `doc_export_text` | Export text |  | `export.text` |
| `doc_create` | Create a PDF |  |  |
| `doc_reduce` | Reduce file size |  | `optimize.reduce` |
| `doc_initial_view` | Initial view |  |  |
| `doc_audit_space` | Audit space usage | RO | `optimize.advanced` |
| `doc_revisions` | List revisions |  |  |
| `doc_open_revision` | Open a revision |  |  |
| `doc_optimize` | Optimize PDF |  | `optimize.advanced` |
| `doc_flatten` | Flatten | destructive |  |
| `doc_inspect` | Inspect open documents | RO |  |

## Pages

| Tool | What it does | Flags | Command |
|---|---|---|---|
| `page_render` | Render a page | RO |  |
| `page_rotate` | Rotate pages |  | `page.rotate` |
| `page_enhance_camera` | Enhance camera image |  | `ocr.enhance_camera` |
| `page_delete` | Delete pages | destructive | `page.delete` |
| `page_move` | Move pages |  |  |
| `page_insert_blank` | Insert a blank page |  | `page.insert_blank` |
| `page_insert_file` | Insert pages from a file |  | `page.insert` |
| `page_extract` | Extract pages |  | `page.extract` |
| `page_number` | Number pages |  |  |
| `page_add_text` | Add text to a page |  | `edit.text` |
| `page_add_image` | Add an image to a page |  | `edit.image` |
| `view_reading_colors` | Set reading colours |  | `a11y.reading_options` |
| `page_replace` | Replace pages |  | `page.replace` |
| `page_duplicate` | Duplicate pages |  | `page.duplicate` |
| `page_set_box` | Set page boxes / crop |  | `page.boxes` |
| `page_images` | List page images | RO | `edit.edit_text` |

## Text, content and images

| Tool | What it does | Flags | Command |
|---|---|---|---|
| `object_list` | List editable objects | RO |  |
| `object_move` | Move objects together |  |  |
| `text_extract` | Extract text | RO | `edit.column_select` |
| `text_find` | Find text | RO | `edit.find` |
| `stamp_custom` | Add a custom stamp |  | `comment.stamp` |
| `content_list` | List added content | RO |  |
| `content_update` | Edit added content |  |  |
| `content_delete` | Delete added content | destructive |  |
| `text_lines` | List text lines | RO | `edit.edit_text` |
| `image_hit` | Hit test page artwork | RO | `edit.edit_text` |
| `image_edit` | Edit an image |  | `edit.edit_text` |
| `image_save` | Save image as | destructive | `edit.edit_text` |
| `text_font_files` | List installed document fonts | RO | `edit.edit_text` |
| `text_font_import` | Load document font |  | `edit.edit_text` |
| `text_fonts` | List document fonts | RO | `edit.edit_text` |
| `text_paragraphs` | List paragraphs | RO | `edit.edit_text` |
| `text_edit_layout` | Measure text draft | RO | `edit.edit_text` |
| `text_edit` | Edit text |  | `edit.edit_text` |

## Comments and Fill & Sign

| Tool | What it does | Flags | Command |
|---|---|---|---|
| `comment_list` | List comments | RO |  |
| `comment_add` | Add a comment |  |  |
| `comment_reply` | Reply to a comment |  |  |
| `comment_set_status` | Set a comment's status |  |  |
| `comment_mark` | Mark a comment with a checkmark |  |  |
| `comment_lock` | Lock a comment |  |  |
| `comments_hide` | Hide all comments |  | `comment.hide_all` |
| `comments_summarize` | Summarize comments |  | `comment.summarize` |
| `comment_edit` | Edit a comment |  |  |
| `comment_image_preview` | Preview image signature layers | RO |  |
| `comment_delete` | Delete a comment | destructive |  |
| `fill_sign_add` | Fill & Sign: type text or place a mark |  | `sign.fill.text` |
| `fill_sign_date_format` | Date format for Fill & Sign |  |  |

## Forms, JavaScript and actions

| Tool | What it does | Flags | Command |
|---|---|---|---|
| `form_fields` | List form fields | RO |  |
| `form_fill` | Fill in form fields |  |  |
| `form_reset` | Clear form | destructive |  |
| `form_add_field` | Prepare form: add a field |  |  |
| `form_set_image` | Set an image field's picture |  |  |
| `form_set_props` | Field properties |  |  |
| `form_tab_order` | Set the tab order |  |  |
| `form_delete_field` | Delete a field | destructive |  |
| `form_merge_data` | Merge data files into spreadsheet |  | `form.merge_data` |
| `js_run` | Run JavaScript |  | `tools.js_console` |
| `js_document_scripts` | Document JavaScripts | RO | `tools.document_js` |
| `js_set_document_script` | Edit a document JavaScript |  | `tools.document_js` |
| `form_set_script` | Set a field's JavaScript |  | `form.prepare` |
| `action_list` | List actions | RO | `actions.wizard` |
| `action_run` | Run an action |  | `actions.wizard` |
| `form_detect_fields` | Detect form fields |  | `form.detect` |
| `form_actions` | Field actions | RO | `form.prepare` |
| `form_set_actions` | Set field actions |  | `form.prepare` |
| `js_enabled` | JavaScript on or off |  |  |

## Bookmarks and links

| Tool | What it does | Flags | Command |
|---|---|---|---|
| `bookmark_list` | List bookmarks | RO |  |
| `bookmark_add` | Add a bookmark |  |  |
| `bookmark_rename` | Rename a bookmark |  |  |
| `bookmark_delete` | Delete a bookmark | destructive |  |
| `bookmark_move` | Move a bookmark |  |  |
| `bookmark_set_page` | Set a bookmark's page |  |  |
| `bookmark_from_structure` | New bookmarks from structure |  |  |
| `link_list` | List links | RO |  |
| `link_open` | Open a linked PDF |  |  |
| `link_add` | Add a link |  | `edit.link` |
| `link_edit` | Edit a link |  |  |
| `link_delete` | Delete a link | destructive |  |
| `links_from_urls` | Create links from URLs |  | `edit.links_from_urls` |
| `links_remove` | Remove all links | destructive | `edit.remove_links` |

## Redaction

| Tool | What it does | Flags | Command |
|---|---|---|---|
| `redact_mark` | Mark for redaction |  |  |
| `redact_apply` | Apply redactions | destructive |  |
| `redact_clear` | Remove redaction marks | destructive |  |

## Signatures

| Tool | What it does | Flags | Command |
|---|---|---|---|
| `sign_list` | List and validate signatures | RO |  |
| `sign_id_create` | Create a digital ID |  |  |
| `sign_windows_ids` | List Windows store digital IDs | RO | `sign.digital` |
| `sign_keychain_ids` | List Keychain digital IDs | RO | `sign.digital` |
| `sign_document` | Sign a document |  | `sign.digital` |
| `sign_trust` | Trust certificates |  |  |

## Accessibility and PDF/A

| Tool | What it does | Flags | Command |
|---|---|---|---|
| `accessibility_autotag_preview` | Preview automatic tags | RO |  |
| `accessibility_check` | Check for accessibility | RO | `a11y.check` |
| `accessibility_report` | Accessibility report | destructive | `a11y.report` |
| `accessibility_review_record` | Accessibility review record | destructive |  |
| `accessibility_review_save` | Save accessibility review decisions | destructive |  |
| `accessibility_review_load` | Open accessibility review decisions | RO |  |
| `accessibility_review_html` | Accessibility review summary | destructive |  |
| `accessibility_fix` | Fix an accessibility problem |  |  |
| `accessibility_figures` | List figures | RO | `a11y.alt_text` |
| `accessibility_set_alt` | Set alternate text |  | `a11y.alt_text` |
| `accessibility_tags` | List structure tags | RO | `a11y.tags` |
| `accessibility_set_tag_property` | Edit tag property |  |  |
| `accessibility_move_tag` | Move structure tag |  |  |
| `pdfa_verify` | Verify PDF/A | RO | `standards.pdfa` |
| `pdfa_convert` | Save as PDF/A |  | `standards.pdfa` |

## Measuring

| Tool | What it does | Flags | Command |
|---|---|---|---|
| `measure_distance` | Measure distance |  | `measure.distance` |
| `measure_perimeter` | Measure perimeter |  | `measure.perimeter` |
| `measure_area` | Measure area |  | `measure.area` |
| `measure_info` | Read a measurement | RO | `measure.info` |
| `measure_list` | List measurements | RO |  |
| `measure_scale` | Set or read a measurement scale |  | `measure.scale` |
| `measure_snap` | Snap a measurement vertex | RO | `measure.snap` |
| `measure_export` | Export measurements as CSV |  | `measure.export` |

## OCR

| Tool | What it does | Flags | Command |
|---|---|---|---|
| `ocr_recognize` | Recognize text (OCR) |  | `ocr.recognize` |
| `ocr_recognize_files` | Recognize text in multiple files |  | `ocr.recognize_batch` |
| `ocr_status` | OCR status | RO | `ocr.recognize` |

## Printing

| Tool | What it does | Flags | Command |
|---|---|---|---|
| `printers` | List printers | RO |  |
| `printer_options` | List printer options | RO |  |
| `print_readiness` | Print readiness | RO |  |

## Undo, commands and previews

| Tool | What it does | Flags | Command |
|---|---|---|---|
| `edit_undo` | Undo |  | `edit.undo` |
| `edit_redo` | Redo |  | `edit.redo` |
| `command_list` | List commands | RO |  |
| `command_run` | Run a command | destructive |  |
| `command_batch` | Run several commands | destructive |  |
| `render_preview` | Render a preview | RO |  |

## Compact-mode meta tools

`pdfcraft-cli mcp --compact` adds `tool_search` (`query`, `category` or `name`) and `tool_call` (`name`, `arguments`). They exist only in compact mode.
