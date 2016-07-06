platform :ios, '10.0'

target 'ValidationTest' do
  
  use_frameworks!
  
 pod 'Alamofire', git: "https://github.com/Alamofire/Alamofire.git", branch: "swift3"

end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      if config.name != 'Debug'
        config.build_settings['SWIFT_OPTIMIZATION_LEVEL'] = '-Owholemodule'
      else
        config.build_settings['SWIFT_OPTIMIZATION_LEVEL'] = '-Onone'
      end
    end
  end
end