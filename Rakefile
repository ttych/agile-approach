# frozen_string_literal: true

require 'fileutils'

include FileUtils

JS_FILES = ['node_modules/jquery/dist/jquery.min.js',
            'node_modules/popper.js/dist/umd/popper.min.js',
            'node_modules/bootstrap/dist/js/bootstrap.min.js']
JS_DIR = 'assets/js/'

CSS_SOURCE = 'node_modules/bootstrap/scss/'
CSS_TARGET = '_sass/bootstrap/'

task :bootstrap do
  `npm install`
  mkdir_p(JS_DIR)
  JS_FILES.each do |file|
    cp(file, JS_DIR)
  end
  rm_rf(CSS_TARGET)
  cp_r(CSS_SOURCE, CSS_TARGET)
end

task :default => :bootstrap
