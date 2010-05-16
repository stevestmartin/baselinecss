desc "Compress CSS files"
task :compress do
  output_file = "css/compressed/baseline.compress.css"
  File.unlink(output_file) if File.exists?(output_file)

  input_files = ["baseline.reset.css", "baseline.base.css", "baseline.grid.css", 
                 "baseline.table.css", "baseline.form.css", "baseline.type.css"]

  input_files.each do |file|
    `java -jar bin/yuicompressor-2.4.2.jar -o #{output_file} css/uncompressed/#{file}`
  end
end
