# NO TIME TO DIE
@extends('erp')
@section('MetaTitle')
<title>Login | Snow Berry ERP</title>
@endsection

@section('styles')
@endsection

@section('content')

	<div>
		<div class="container mx-auto">
			<div class="grid grid-cols-1 md:grid-cols-12 gap-4 items-center justify-between">
				<div class="lg:col-span-7 md:col-span-6 md:block d-none">
					<div class="p-2 h-[100vmin] overflow-hidden">
						<img src="{{ asset('images/bg-login.png') }}" alt="bg-login" class="w-full h-full rounded-[20px] object-cover object-center">
					</div>
				</div>
				<div class="lg:col-span-4 md:col-span-6 col-span-4 md:pl-0 px-5 md:mb-0 mb-5">
					<form action="" method="post" class="bg-white rounded-[20px] p-10">
						<img src="{{ asset('images/logo.svg') }}" alt="logo" class="w-[228px] mx-auto mb-3">
						<h1 class="text-2xl text-blueCrayola text-center mb-5">ERP LOG IN</h1>
						<h1 class="text-1xl text-blueCrayola mb-0">Welcome Back :)</h1>
						<p class="text-eerieBlack mb-5 text-sm">Enter your credentials to access your account</p>
						<h6 class="text-eerieBlack mb-2 text-sm">Choose your role</h6>
						<div class="bg-quickSilver inline-flex px-0 rounded-[10px] mb-5">
							<label class="inline-flex items-center">
								<input type="radio" name="role" value="Admin" id="adminRadio" class="appearance-none">
								<button type="button" class="btn-web" onclick="updateRadio('adminRadio')">
									Admin
								</button>
							</label>
							<label class="inline-flex items-center">
								<input type="radio" name="role" value="User" id="userRadio" class="appearance-none">
								<button type="button" class="btn-web" onclick="updateRadio('userRadio')">
									User
								</button>
							</label>
						</div>
						<div>
							<label class="inline-block mb-2 text-sm">Log in ID</label>
							<input type="text" name="login_id" class="form-control mb-5" placeholder="eg. 21354" />
							<label class="inline-block mb-2">
								<span class="mr-5 text-sm">Password</span>
								<small class="px-5 pt-0 pb-1 small bg-platinum rounded-[12px]">Log in with Pin</small>
							</label>
							<div class="relative">
								<input type="password" name="password" class="form-control mb-5 pr-5 passwordField" placeholder="eg. ABCD@1234" />
								<div class="absolute top-0 right-0 bottom-0 flex items-center px-3 togglePassword">
									<img src="{{ asset('images/icons/icon-eye.svg') }}" alt="icon-eye">
								</div>
							</div>
							<div class="md:flex items-center justify-between mb-5">
								<label for="rememberPin" class="flex items-center">
									<input type="checkbox" id="rememberPin" class="mb-0 mr-1" />
									<small class="mb-0 text-sm">Use only Pin/Password for next time</small>
								</label>
								<a href="javascript:void(0)" class="text-blueBolt"><small>Forgot password?</small></a>
							</div>
							<button type="submit" class="btn-web bg-blueCrayola w-full mb-5">Log In</button>
							<span class="mb-0 border-l block text-center">Powered by SnowBerry</span>
						</div>
					</form>
				</div>
			</div>
		</div>
	</div>

@endsection

@section('scripts')
<script type="text/javascript">
	function updateRadio(radioId) {
		const radio = document.getElementById(radioId);
		radio.checked = true;
	}
</script>
@endsection
