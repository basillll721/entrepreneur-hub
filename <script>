import { createClient } from 'https://cdn.jsdelivr.net/npm/@supabase/supabase-js/+esm'

const supabaseUrl = 'https://YOUR-PROJECT-URL.supabase.co'
const supabaseKey = 'YOUR-ANON-KEY'
const supabase = createClient(supabaseUrl, supabaseKey)
async function getUser() {
  const { data: { user } } = await supabase.auth.getUser()
  if (user) {
    document.getElementById('user-info').style.display = 'block'
    document.getElementById('user-email').innerText = `Logged in as: ${user.email}`
  }
}

getUser();

async function signOut() {
  await supabase.auth.signOut()
  window.location.reload()
}
