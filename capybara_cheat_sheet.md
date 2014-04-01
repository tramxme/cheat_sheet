=Navigating=

    visit('/projects')
    visit(post_comments_path(post))
 
=Clicking links and buttons=

    click_link('id-of-link')
    click_link('Link Text')
    click_button('Save')
    click('Link Text') # Click either a link or a button
    click('Button Value')
    click_on("Name")
    find_link('Name').click #Or .trigger('click')
    find_button('Name').click
    find(xpath/css).click
 
=Interacting with forms=

    fill_in('First Name', :with => 'John')
    fill_in('Password', :with => 'Seekrit')
    fill_in('Description', :with => 'Really Long Text…')
    choose('A Radio Button')
    check('A Checkbox')
    uncheck('A Checkbox')
    attach_file('Image', '/path/to/image.jpg')
    select('Option', :from => 'Select Box')
 
=scoping=

    within("//li[@id='employee']") do
      fill_in 'Name', :with => 'Jimmy'
    end
    within(:css, "li#employee") do
      fill_in 'Name', :with => 'Jimmy'
    end
    within_fieldset('Employee') do
      fill_in 'Name', :with => 'Jimmy'
    end
    within_table('Employee') do
      fill_in 'Name', :with => 'Jimmy'
    end
     
=Querying=

    page.has_xpath?('//table/tr')
    page.has_css?('table tr.foo')
    page.has_content?('foo')
    page.should have_xpath('//table/tr')
    page.should have_css('table tr.foo')
    page.should have_content('foo')
    page.should have_no_content('foo')
    find_field('First Name').value
    find_link('Hello').visible?
    find_button('Send').click
    find('//table/tr').click
    locate("//*[@id='overlay'").find("//h1").click
    all('a').each { |a| a[:href] }
 
=Scripting=

    result = page.evaluate_script('4 + 4');
    page.execute_script('1+1')
 
=Debugging=

    save_and_open_page
    screenshot_and_open_image #(install gem Capybara_screenshot)
    page.driver.render('random_name.png', full: true)
    pry #(install gem pry)
    debugger #(install gem debugger)
 
=Asynchronous JavaScript=

    find_link('foo').click
    page.should have_content('baz')
    page.should_not have_xpath('//a')
    page.should have_no_xpath('//a')
 
=XPath and CSS=
    within(:css, 'ul li') { ... }
    find(:css, 'ul li').text
    locate(:css, 'input#name').value #For input, use .value. Other fields, use .text
    Capybara.default_selector = :css
    within('ul li') { ... }
    find('ul li').text
    locate('input#name').value
