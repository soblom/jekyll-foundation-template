require 'rake'

js_files = FileList.new(
    'bower_components/jquery/dist/jquery.min.js',
    'bower_components/jquery/dist/jquery.min.map',
    'bower_components/foundation/js/foundation.min.js',
    'bower_components/modernizr/modernizr.js'
  )

desc 'copies required Foundation js-files into right place for being build'
task :cp_foundation_js do
  FileUtils.mkdir_p("js")
  js_files.each do |f|
    FileUtils.cp(f, "js/#{File.basename(f)}")
  end
end
