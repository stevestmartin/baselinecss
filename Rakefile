desc "Compress CSS files"
task :compress do
  output_file = File.new("css/compressed/baseline.compress.css", File::CREAT|File::TRUNC|File::RDWR, 0644)

  input_files = ["baseline.reset.css", "baseline.base.css", "baseline.grid.css", "baseline.table.css", "baseline.form.css", "baseline.type.css"]
  input_files.each do |file|
    output_file.write(`java -jar bin/yuicompressor-2.4.2.jar css/uncompressed/#{file}`)
  end
end
